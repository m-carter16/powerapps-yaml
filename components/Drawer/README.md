# Drawer Component

A reusable side drawer component for PowerApps that slides in from the left or right side of the screen with customizable content, loading states, and action buttons.

## Features

- **Side navigation** that slides in from left or right
- **Configurable direction** (left/right side)
- **Semi-transparent overlay** background
- **Customizable header** with title and close button
- **Loading state** with spinner animation
- **Action buttons** (Cancel/Confirm) with customizable logic
- **Responsive design** that adapts to screen size
- **Context variables** for state management

## Installation

1. Copy the YAML content from `drawer.yml` between the START and END markers
2. In PowerApps Studio, select the screen where you want to add the Drawer
3. Press Ctrl+V to paste
4. The Drawer will appear on your screen ready to use

## Usage

### Opening the Drawer
Use the provided button or trigger the drawer programmatically:

**Right-side drawer:**
```powerpoint
UpdateContext({
    locDrawer: {
        Type: "right",
        Open: true
    },
    locDrawerLoading: false
})
```

**Left-side drawer:**
```powerpoint
UpdateContext({
    locDrawer: {
        Type: "left", 
        Open: true
    },
    locDrawerLoading: false
})
```

### Closing the Drawer
```powerpoint
UpdateContext({locDrawer: {open: false}})
```

### Showing Loading State
```powerpoint
UpdateContext({locDrawerLoading: true})
```

## Context Variables

- `locDrawer` (Record): Contains Type ("left"/"right") and Open (Boolean) properties
- `locDrawerLoading` (Boolean): Controls loading state display

## Customization

- **Drawer Side**: Set `locDrawer.Type` to "left" or "right"
- **Header Text**: Modify the `lblSidedDrawerHeader` Text property
- **Body Content**: Add content to `cntSidedDrawerBody` container
- **Loading Message**: Update the `spnSidedDrawerLoad` Label property
- **Button Actions**: Customize the OnSelect properties of action buttons
- **Styling**: Adjust colors, sizes, and spacing in the Properties sections

## Components Structure

- `btnOpenDrawer`: Trigger button to open the drawer
- `cntDrawerBackground`: Main drawer background with overlay
- `cntDrawer`: Drawer container
- `cntSidedDrawerHeader`: Header with title and close button
- `cntSidedDrawerBody`: Main content area (add your content here)
- `cntSidedDrawerLoad`: Loading state container
- `cntSidedDrawerActions`: Action buttons container

## Tips

- The drawer automatically positions itself on the correct side based on the Type setting
- Use the body container (`cntSidedDrawerBody`) to add your custom content
- The loading state will hide the main content and show a spinner
- Customize button actions to perform your specific business logic before closing
