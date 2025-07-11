# FeaturedButton Component

A reusable featured button component for PowerApps that displays an icon, title, and description in a clean card-style layout with click functionality.

## Features

- **Icon display** with customizable SVG graphics
- **Title and description** text with proper typography
- **Card-style design** with subtle drop shadow
- **Responsive layout** with auto-sizing text
- **Click functionality** with customizable OnSelect action
- **Professional styling** using app theme colors
- **Horizontal layout** with icon on left, content on right

## Installation

1. Copy the YAML content from `FeaturedButton.yml`
2. In PowerApps Studio, select the screen where you want to add the FeaturedButton
3. Press Ctrl+V to paste
4. The FeaturedButton will appear on your screen ready to use

## Usage

### Basic Implementation
The FeaturedButton is ready to use immediately after pasting. It includes:
- A sample icon (rocket/launch icon)
- Default title "Title" 
- Default description "Description of what this button is doing"
- Click notification for testing

### Customizing Content
Update the text properties:
```powerpoint
// Title
lblFeaturedButtonTitle_FB.Text = "Your Title"

// Description  
lblFeaturedButtonDescription_FB.Text = "Your description text"
```

### Customizing the Icon
The component uses an SVG icon embedded as a data URI. To change the icon:

1. **Using PowerIcons (Recommended):**
   - Visit [PowerIcons.dev](https://www.powericons.dev/)
   - Browse or search for your desired icon
   - Customize colors, stroke width, or rotation as needed
   - Click the icon to copy its YAML code
   - Replace the `Image` property of `imgFeaturedButton_FB` with the copied code

2. **Using External SVGs:**
   - Go to [PowerIcons.dev](https://www.powericons.dev/) and click "External SVG"
   - Paste your SVG code into the text area
   - Customize colors if needed using the color analyzer
   - Convert & copy the PowerApps-friendly YAML
   - Replace the `Image` property of `imgFeaturedButton_FB`

### PowerIcons Instructions
For detailed instructions on using PowerIcons, visit: [PowerIcons Instructions](https://www.powericons.dev/instructions)

> **💡 Fluent Design Tip:** When browsing icons on PowerIcons.dev, use the **Fluent 2** filter to maintain consistency with PowerApps' Fluent Design system. This ensures your components follow Fluent design guidelines.

**Quick Steps:**
1. Browse icons on [PowerIcons.dev](https://www.powericons.dev/)
2. **Set the filter to "Fluent 2"** to match PowerApps design standards
3. Click any icon to copy its YAML code
4. In PowerApps, replace the `Image` property of `imgFeaturedButton_FB`
5. Remember to select "Paste code" when prompted in PowerApps

### Customizing Click Action
Update the OnSelect property of `btnFeaturedButton_FB`:
```powerpoint
// Navigate to another screen
Navigate(YourTargetScreen, ScreenTransition.Fade)

// Show a form
UpdateContext({showForm: true})

// Launch a URL
Launch("https://your-url.com")

// Custom logic
Set(yourVariable, "value");
// Add more actions as needed
```

## Styling Customization

### Colors
- **Title Color**: Modify `lblFeaturedButtonTitle_FB.FontColor`
- **Background**: Change `cntFeaturedButton_FB.Fill`
- **Icon Color**: Update the SVG fill color in the Image property

### Sizing
- **Component Size**: Adjust `cntFeaturedButton_FB.Height` and `Width`
- **Icon Size**: Modify `imgFeaturedButton_FB.Height` (width auto-adjusts)
- **Text Size**: Update font sizes in the label properties

### Layout
- **Padding**: Adjust padding properties in `cntFeaturedButtonBody_FB`
- **Spacing**: Modify `LayoutGap` for space between icon and text
- **Shadow**: Customize `DropShadow` property

## Components Structure

- `cntFeaturedButton_FB`: Main container with card styling
- `cntFeaturedButtonBody_FB`: Inner container with horizontal layout
- `imgFeaturedButton_FB`: Icon image component
- `cntFeaturedButtonLabels_FB`: Text container with vertical layout
- `lblFeaturedButtonTitle_FB`: Title text (bold, themed color)
- `lblFeaturedButtonDescription_FB`: Description text (medium weight)
- `btnFeaturedButton_FB`: Invisible button overlay for click handling

## Integration Tips

- **Navigation Cards**: Use for main menu or dashboard navigation
- **Feature Highlights**: Showcase key app features or capabilities  
- **Action Cards**: For primary user actions or workflows
- **Settings Options**: Create settings or configuration menus
- **Gallery Items**: Use in galleries for list-style navigation

## Icon Resources

- **PowerIcons**: [https://www.powericons.dev/](https://www.powericons.dev/) - Comprehensive icon library for PowerApps
- **Instructions**: [PowerIcons Usage Guide](https://www.powericons.dev/instructions)
- **Custom SVGs**: Import your own SVG graphics using the External SVG tool
- **Icon Libraries**: Heroicons, Feather Icons, and other SVG icon sets can be converted

## Accessibility

- Ensure sufficient color contrast for text readability
- Use descriptive titles and descriptions
- Consider adding `AccessibleLabel` properties for screen readers
- Test with keyboard navigation if needed
