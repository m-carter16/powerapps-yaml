# PowerApps Fluent Design YAML Component Library

A comprehensive YAML component library for PowerApps Canvas Apps that implements Fluent UI React v9 design patterns and components.

## Overview

This library provides ready-to-use YAML snippets for PowerApps Canvas Apps that closely mirror the design, behavior, and styling of Microsoft's Fluent UI React v9 components. Each component is crafted to maintain visual consistency and user experience patterns while working within PowerApps' capabilities.

## Features

- 🎨 **Fluent UI v9 Compliance**: Components designed to match Fluent UI React v9 specifications
- 📱 **Responsive Design**: Components that adapt to different screen sizes
- 🎯 **Accessibility Ready**: Built with accessibility best practices
- 🔧 **Easy Integration**: Simple copy-paste YAML snippets
- 📖 **Comprehensive Documentation**: Detailed usage examples and customization guides

## Component Library

### Available Components

For a complete list of available components, see [COMPONENTS.md](COMPONENTS.md).

#### Currently Available (v1.1.0)
- **Dialog** - A centered dialog component with background overlay
- **Drawer** - A side panel component that can open from left or right
- **SearchBox** - A search input component with icon and clear functionality  
- **FeaturedButton** - A card-like button with title, description, and icon
- **TimePicker** - A time selection component with support for 12-hour and 24-hour formats

### Component Development Status
- ✅ **Complete**: 5 components fully implemented with documentation
- 📋 **Planned**: Additional Input, Navigation, and Feedback components (see [COMPONENTS.md](COMPONENTS.md) for roadmap)

### Component Structure

Each component follows a standardized structure:
```
components/
├── component-name/
│   ├── component-name.yml          # Main component YAML
│   └── README.md                   # Component documentation
```

## Quick Start

### Using Components

1. **Browse Components**: Check [COMPONENTS.md](COMPONENTS.md) for a complete list of available components
2. **Navigate to Component**: Go to the component directory (e.g., `components/SearchBox/`)
3. **Copy YAML**: Open the `.yml` file and copy the YAML content
4. **Paste in PowerApps**: In PowerApps Studio, select your target screen and press `Ctrl+V`
5. **Customize**: Modify properties like width, height, colors, and behavior as needed

## Documentation

- **Component List**: [COMPONENTS.md](COMPONENTS.md) - Complete list of components with descriptions and roadmap
- **Version History**: [CHANGELOG.md](CHANGELOG.md) - Detailed version history and release notes
- **Individual Components**: Each component includes its own README with detailed usage examples
