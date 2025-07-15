# Header Component

A reusable header canvas component for PowerApps that displays a primary title and secondary description text in a clean, centered layout with branded styling.

## Features

- **Dual-text display** with primary title and secondary description
- **Centered alignment** for professional presentation
- **Branded styling** using app theme primary color background
- **Responsive layout** with auto-sizing text
- **Full-width design** that spans the entire app width
- **Typography hierarchy** with bold title and italic description
- **Professional color scheme** with white text on primary background

## Properties

| Name | Type | Description |
|------|------|-------------|
| PrimaryText | Input | Main title text displayed prominently at the top |
| SecondaryText | Input | Description text displayed below the title |

## Installation

1. Copy the YAML content from `Header.yml`
2. In PowerApps Studio, select the screen where you want to add the Header
3. Press Ctrl+V to paste
4. The Header will appear on your screen ready to use

## Usage

### Basic Implementation
The Header is ready to use immediately after pasting. It includes:
- Default primary text "Monthly Roadmap Dashboard"
- Default secondary text "Highly Confidential - Internal Only"
- Full app width spanning design
- Primary theme color background

### Customizing Content
Update the component properties directly in PowerApps:
```powerpoint
// Primary Title
Set(Header1.PrimaryText, "Your App Title")

// Secondary Description  
Set(Header1.SecondaryText, "Your subtitle or description")
```

### Common Use Cases
- **App Headers**: Main application title and branding
- **Page Headers**: Section titles with descriptions
- **Dashboard Headers**: Dashboard names with classification labels
- **Report Headers**: Report titles with confidentiality notices
- **Screen Titles**: Individual screen identification

## Styling Customization

### Colors
- **Background Color**: Modify the component's `Fill` property (defaults to `App.Theme.Colors.Primary`)
- **Text Color**: Both title and description use white text (`RGBA(255, 255, 255, 1)`)
- **Theme Integration**: Automatically uses your app's primary theme color

### Typography
- **Primary Text**: 24pt bold font, centered alignment
- **Secondary Text**: 16pt regular italic font, centered alignment
- **Font Family**: Uses PowerApps default font family

### Sizing
- **Component Height**: Fixed at 70px for consistent header sizing
- **Component Width**: Spans full app design width (`App.DesignWidth`)
- **Text Heights**: Primary text (35px), secondary text auto-sized

### Layout
- **Alignment**: Both texts are center-aligned horizontally and vertically
- **Spacing**: Vertical auto-layout with stretch alignment
- **Positioning**: Full-width header typically placed at top of screen

## Component Structure

- `Header`: Main component container with primary color background
- `ctr_Header`: Auto-layout container for vertical text arrangement
- `lblHeaderTitle`: Primary title text (bold, large font)
- `lblHeaderDescription`: Secondary description text (italic, smaller font)

## Integration Tips

- **Screen Headers**: Place at the top of each screen for consistent branding
- **Navigation Context**: Use secondary text to show current section or page
- **Classification Labels**: Use secondary text for security or confidentiality notices
- **Responsive Design**: Component automatically adjusts to app width changes
- **Theme Consistency**: Automatically inherits app theme primary color
- **Typography Hierarchy**: Built-in text sizing creates clear information hierarchy

## Customization Examples

### App Branding
```powerpoint
// Company app header
PrimaryText: "Contoso Analytics Platform"
SecondaryText: "Real-time Business Intelligence Dashboard"
```

### Page Context
```powerpoint
// Section-specific header
PrimaryText: "Employee Management"
SecondaryText: "Human Resources Portal - Internal Use Only"
```

### Dashboard Header
```powerpoint
// Executive dashboard
PrimaryText: "Executive Dashboard"
SecondaryText: "Q4 2024 Performance Metrics - Confidential"
```

### Classification Notice
```powerpoint
// Security classification
PrimaryText: "Financial Reports"
SecondaryText: "Restricted Access - Finance Team Only"
```

## Design Guidelines

- **Text Length**: Keep primary text concise (1-5 words recommended)
- **Secondary Text**: Use for context, classification, or brief descriptions
- **Consistency**: Use consistent header styling across all app screens
- **Accessibility**: High contrast white text on primary color background
- **Branding**: Leverage theme colors for consistent brand presentation
- **Hierarchy**: Primary text should be the main identifier, secondary provides context

## Accessibility

- High contrast color scheme (white text on dark primary background)
- Clear typography hierarchy with appropriate font sizes
- Center alignment ensures readability across different screen sizes
- Consider adding `AccessibleLabel` properties for screen readers
- Ensure primary theme color provides sufficient contrast for text readability
