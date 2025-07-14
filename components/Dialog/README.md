# Dialog Component

A reusable dialog component for PowerApps that provides a modal overlay with customizable content, loading states, and action buttons.

## Features

- **Modal overlay** with semi-transparent background
- **Customizable header** with title and close button
- **Loading state** with spinner animation
- **Action buttons** (Cancel/Confirm) with customizable logic
- **Responsive design** that centers on screen
- **Context variables** for state management

## Installation

1. Copy the YAML content from `dialog.yml` between the START and END markers
2. In PowerApps Studio, select the screen where you want to add the Dialog
3. Press Ctrl+V to paste
4. The Dialog will appear on your screen ready to use

## Usage

### Opening the Dialog
Use the provided button or trigger the dialog programmatically:
```powerpoint
UpdateContext({
    locDialogOpen: true,
    locDialogLoading: false
})
```

### Closing the Dialog
```powerpoint
UpdateContext({locDialogOpen: false})
```

### Showing Loading State
```powerpoint
UpdateContext({locDialogLoading: true})
```

## Context Variables

- `locDialogOpen` (Boolean): Controls dialog visibility
- `locDialogLoading` (Boolean): Controls loading state display

## Customization

- **Header Text**: Modify the `lblCenteredDialogHeader` Text property
- **Body Content**: Replace `lblConfirmCentered` with your own content
- **Loading Message**: Update the `spnCenteredDialogLoad` Label property
- **Button Actions**: Customize the OnSelect properties of action buttons
- **Styling**: Adjust colors, sizes, and spacing in the Properties sections

## Components Structure

- `btnOpenDialog`: Trigger button to open the dialog
- `ctrDialog`: Main dialog container with overlay
- `ctrCenteredDialog`: Centered dialog box
- `ctrCenteredDialogHeader`: Header with title and close button
- `ctrCenteredDialogBody`: Main content area
- `ctrCenteredDialogLoad`: Loading state container
- `ctrCenteredDialogActions`: Action buttons container
