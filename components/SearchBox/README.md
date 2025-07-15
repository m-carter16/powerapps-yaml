# SearchBox Component

A reusable search input canvas component for PowerApps with search icon, text input field, and clear button functionality.

## Features

- **Search icon** for visual clarity
- **Text input field** with search type styling
- **Clear button** that appears when text is entered
- **Auto-reset functionality** when clear button is pressed
- **Responsive design** with customizable dimensions
- **Clean border styling** with rounded corners
- **Context variable integration** for state management

## Properties

| Name | Type | Description |
|------|------|-------------|
| Value | Output | Outputs the search text value to be used in the parent app |
| UseFilterIcon | Input (Boolean) | Set to true to use filter icon instead of the search icon |
| IconColor | Input (Color) | Changes the color of the icons (Search or Filter, Cancel) |

## Installation

1. Copy the YAML content from `searchbox.yml`
2. In your PowerApps canvas app, click the components tab
3. Press Ctrl+V to paste. You do not need to create new component. It will paste as a new component.
4. Your component is now ready to be added to any screen of your app. 
5. If you want to use filter icon, set the UseFilterIcon to true
6. If you want to change the color of the icon, set IconColor to desired color.
7. You can use the "Value" property of the component to filter/search your collection.

## Usage

### Basic Implementation
The SearchBox is ready to use immediately after pasting. The search input will:
- Show a search icon on the left
- Accept text input in the center
- Display a clear button (X) on the right when text is present

### Accessing Search Value
Use the component's `Value` output property in your formulas:
```powerpoint
SearchBox1.Value
```

### Handling Search Logic
Add your search logic to the `OnChange` property or create a separate search button:
```powerpoint
// In OnChange property (real-time search)
UpdateContext({showClearButton: !IsBlank(Self.Value)});
// Add your search logic here
Filter(YourDataSource, SearchColumn in SearchBox1.Value)
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
