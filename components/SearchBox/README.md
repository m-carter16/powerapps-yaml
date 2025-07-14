# SearchBox Component

A reusable search input component for PowerApps with search icon, text input field, and clear button functionality.

## Features

- **Search icon** for visual clarity
- **Text input field** with search type styling
- **Clear button** that appears when text is entered
- **Auto-reset functionality** when clear button is pressed
- **Responsive design** with customizable dimensions
- **Clean border styling** with rounded corners
- **Context variable integration** for state management

## Installation

1. Copy the YAML content from `searchbox.yml` between the START and END markers
2. In PowerApps Studio, select the screen where you want to add the SearchBox
3. Press Ctrl+V to paste
4. The SearchBox will appear on your screen ready to use

## Usage

### Basic Implementation
The SearchBox is ready to use immediately after pasting. The search input will:
- Show a search icon on the left
- Accept text input in the center
- Display a clear button (X) on the right when text is present

### Accessing Search Value
Use the text input control's value in your formulas:
```powerpoint
txtSearchInput.Value
```

### Handling Search Logic
Add your search logic to the `OnChange` property or create a separate search button:
```powerpoint
// In OnChange property (real-time search)
UpdateContext({showClearButton: !IsBlank(Self.Value)});
// Add your search logic here
Filter(YourDataSource, SearchColumn in txtSearchInput.Value)
```

### Clearing the Search
The clear button automatically resets the input:
```powerpoint
Reset(txtSearchInput); 
UpdateContext({showClearButton: false})
```

## Context Variables

- `showClearButton` (Boolean): Controls clear button visibility (auto-managed)

## Customization

### Styling
- **Size**: Modify `Height` and `Width` properties of `ctrSearchBox`
- **Position**: Adjust `X` and `Y` coordinates
- **Colors**: Change `BorderColor` and `Fill` properties
- **Border**: Customize `BorderThickness` and radius properties
- **Font**: Update `Font` and `FontSize` in `txtSearchInput`

### Functionality
- **Placeholder Text**: Add `HintText` property to `txtSearchInput`
- **Search Logic**: Enhance the `OnChange` property with your search implementation
- **Icon**: Change the `Icon` property of `icoSearch` to a different icon
- **Clear Behavior**: Modify the `OnSelect` property of `btnClear`

### Responsive Design
Adjust the positioning and sizing of child elements:
- `icoSearch`: Search icon positioning (X=6, Y=6)
- `txtSearchInput`: Main input field (X=28, Y=2)
- `btnClear`: Clear button positioning (X=294, Y=6)

## Components Structure

- `ctrSearchBox`: Main container with border styling
- `icoSearch`: Search icon on the left
- `txtSearchInput`: Text input field in the center
- `btnClear`: Clear button on the right (visible when text exists)

## Integration Tips

- Use with galleries or data tables for filtering
- Connect to SharePoint lists or other data sources
- Implement debouncing for performance with large datasets
- Consider adding search suggestions or autocomplete functionality
- Style to match your app's theme and branding
