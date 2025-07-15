# Nav Component

A reusable navigation sidebar canvas component for PowerApps with expandable/collapsible functionality, customizable menu items, and user display options.

## Features

- **Expandable/Collapsible** sidebar with smooth transitions
- **Customizable menu items** with icons, labels, and navigation actions
- **Section headers** for organizing navigation groups
- **User display** with full name integration
- **Responsive design** that adapts to expanded/collapsed states
- **Icon-only view** when collapsed for space efficiency
- **Navigation actions** with screen routing support
- **Hover and press effects** for interactive feedback

## Properties

| Name | Type | Description |
|------|------|-------------|
| Expanded | Input | Controls whether the navigation panel is expanded (true) or collapsed (false) |
| Items | Input | Table of navigation items with id, isHeader, labelText, itemIcon, and screen properties |
| OpenPanelWidth | Input | Width of the navigation panel when expanded |
| ShowUser | Input | Controls whether the user information is displayed at the bottom |

## Installation

1. Copy the YAML content from `navcomponent.yml` between the START and END markers
2. In PowerApps Studio, select the screen where you want to add the Nav component
3. Press Ctrl+V to paste
4. The Nav component will appear on your screen ready to use

## Usage

### Basic Implementation
The Nav component is ready to use immediately after pasting. The navigation will:
- Display as a collapsed sidebar showing only icons
- Expand when the `Expanded` property is set to true
- Show user information at the bottom when expanded (if `ShowUser` is true)
- Navigate to specified screens when menu items are clicked

### Configuring Menu Items
Customize the navigation items by modifying the `Items` property:
```powerpoint
Table(
  { id: 1, isHeader: true, labelText: "Main", itemIcon: Blank(), screen: Blank() },
  { id: 2, isHeader: false, labelText: "Home", itemIcon: Icon.Home, screen: HomeScreen }, 
  { id: 3, isHeader: false, labelText: "Dashboard", itemIcon: Icon.Waffle, screen: DashboardScreen },
  { id: 4, isHeader: false, labelText: "Analytics", itemIcon: Icon.Globe, screen: AnalyticsScreen }
)
```

### Controlling Expansion
Toggle the navigation panel programmatically:
```powerpoint
// Expand the navigation
UpdateContext({navExpanded: true});
Set(Nav1.Expanded, navExpanded)

// Collapse the navigation
UpdateContext({navExpanded: false});
Set(Nav1.Expanded, navExpanded)
```

### Handling Navigation
Navigation actions are handled automatically when menu items have a `screen` property defined. The component will navigate to the specified screen when an item is selected.

## Item Structure

Each item in the `Items` table should have the following properties:
- `id` (Number): Unique identifier for the item
- `isHeader` (Boolean): Whether the item is a section header (true) or navigation item (false)
- `labelText` (Text): Display text for the item
- `itemIcon` (Icon): Icon to display (use `Blank()` for headers)
- `screen` (Screen): Target screen for navigation (use `Blank()` for headers)

## Customization

### Styling
- **Panel Width**: Modify the `OpenPanelWidth` property to adjust expanded width
- **Colors**: Update the `Fill` property to change the background color
- **User Display**: Toggle the `ShowUser` property to show/hide user information
- **Icons**: Change individual item icons in the `Items` table
- **Fonts**: Customize font properties in the text controls

### Functionality
- **Navigation Logic**: Modify the `OnSelect` property of `btnItemAction` for custom navigation behavior
- **Hover Effects**: Adjust `HoverFill` and `PressedFill` properties for different interaction styles
- **Animation**: Add transitions by modifying the `Width` property with animation functions
- **User Information**: Customize the user display in the `conUser` container

### Responsive Design
The component automatically adjusts its layout based on the `Expanded` state:
- **Collapsed**: Shows only icons in a narrow sidebar
- **Expanded**: Shows full labels and user information
- **Icon Alignment**: Automatically centers icons when collapsed, left-aligns when expanded

## Component Structure

- `conUser`: User information container (bottom section)
- `conItems`: Main navigation items container
- `galSideBarItems`: Gallery displaying navigation items
- `lblSectionHeader`: Section header labels
- `conClickableItem`: Clickable navigation item container
- `icoItem`: Navigation item icons
- `lblNavLabel`: Navigation item labels
- `btnItemAction`: Invisible button handling click actions

## Integration Tips

- Use with a hamburger menu button to control the `Expanded` property
- Integrate with screen navigation and app routing
- Consider adding animation transitions for smooth expand/collapse
- Customize colors to match your app's theme and branding
- Use section headers to organize related navigation items
- Test navigation on different screen sizes for optimal user experience
