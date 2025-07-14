# Components Library

## Available Components

#### Dialog
**Location**: `components/dialog.yml`  
**Description**: A dialog component that displays a centered dialog with a button click (local variable change) with a background to prevent clicking outside the dialog.

#### Drawer
**Location**: `components/drawer.yml`  
**Description**: A drawer component that displays a side panel with a button click (local variable change) with a background to prevent clicking outside the panel. Ability to open either from the right or left.

#### SearchBox
**Location**: `components/searchbox.yml`  
**Description**: A search input component with icon and clear functionality

## Planned Components

### Input Components
- [ ] TimePicker - Time selection component
- [ ] CheckboxGroup - Multiple related checkboxes
- [ ] Switch - Toggle switch component

### Button Components
- [ ] FeaturedButton - Button similar to a card with title, description and icon (useful on home screen)
- [ ] MenuButton - Button that opens a menu
- [ ] SplitButton - Button with dropdown action

### Navigation Components
- [ ] Breadcrumb - Navigation breadcrumb trail
- [ ] Nav - Vertical navigation menu
- [ ] TabList - Horizontal tab navigation
- [ ] Pagination - Page navigation component

### Feedback Components
- [ ] MessageBar - Informational message banner
- [ ] Toast - Temporary notification popup

### Data Display Components
- [ ] Avatar - User profile image/initials
- [ ] Badge - Small status or count indicator

## Component Lifecycle

### Development Status Legend
- ✅ **Complete**: Fully implemented with documentation and examples
- 🚧 **In Progress**: Currently being developed
- 📋 **Planned**: Scheduled for future development
- 🔄 **Needs Update**: Requires updates for latest Fluent UI specs

### Version History

#### v1.0.0 (Current)
- ✅ SearchBox
- ✅ Dialog
- ✅ Drawer
- ✅ FeatureButton

#### v1.1.0 (Planned)
- 📋 Input Components

#### v1.2.0 (Planned)
- 📋 Selection components
- 📋 Navigation components

---

## Quick Start Guide

### 1. Choose a Component
Browse the available components above and select the one you need.

### 2. Copy the YAML
Navigate to the component file and copy the YAML content.

### 3. Paste in PowerApps
Paste the YAML into your PowerApps Canvas App.

### 4. Customize
Modify properties like width, height, colors, and behavior as needed.

### 5. Test
Verify functionality and accessibility in your app.

---

## Contributing

### Adding New Components

When contributing new components, ensure they include:

1. **Main Component File** - Core YAML implementation
2. **README.md** - Comprehensive documentation
3. **Variants** - Size and theme variations
4. **Examples** - Real-world usage scenarios
5. **Accessibility** - Full keyboard and screen reader support

### Quality Standards

All components must meet these standards:

- ✅ Fluent UI v9 design compliance
- ✅ Accessibility (WCAG 2.1 AA)
- ✅ Keyboard navigation support
- ✅ Responsive design principles
- ✅ Performance optimization
- ✅ Cross-browser compatibility

### Review Process

1. **Design Review**: Verify Fluent UI v9 compliance
2. **Code Review**: Check YAML structure and formulas
3. **Accessibility Review**: Test with screen readers and keyboard
4. **Documentation Review**: Ensure comprehensive documentation
5. **Testing**: Verify across different scenarios and devices

---

## Support and Resources

### Documentation
- **Component Guide**: `docs/GUIDE.md` - Comprehensive usage guide
- **Design Tokens**: `themes/` - Color, typography, and spacing specifications
- **Examples**: `components/*/examples/` - Real-world implementations

### External Resources
- [Fluent UI React v9 Documentation](https://react.fluentui.dev/)
- [Web Content Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

### Community
- Submit issues and feature requests via GitHub
- Contribute components and improvements
- Share usage examples and best practices
