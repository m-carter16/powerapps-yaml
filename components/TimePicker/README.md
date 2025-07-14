# TimePicker Component

A reusable time picker component for PowerApps that provides an intuitive interface for selecting hours and minutes with support for both 12-hour and 24-hour (military) time formats.

## Features

- **Dual time format support** - Toggle between 12-hour (AM/PM) and 24-hour (military) time
- **Hour and minute dropdowns** with proper value ranges
- **Required field indicator** with customizable asterisk display
- **Accessible design** with proper labels and validation states
- **Responsive layout** that adapts to time format selection
- **Auto-layout containers** for consistent spacing and alignment
- **Default time values** (12:00 AM for 12-hour, 00:00 for 24-hour)

## Installation

1. Copy the YAML content from `TimePicker.yml`
2. In PowerApps Studio, select the screen where you want to add the TimePicker
3. Press Ctrl+V to paste
4. The TimePicker will appear on your screen ready to use

## Usage

### Basic Implementation
The TimePicker is ready to use immediately after pasting. It includes:
- A label "Time Picker" with required field indicator (*)
- Hour dropdown with appropriate range based on time format
- Minute dropdown with 00-59 values
- AM/PM dropdown (hidden in military time mode)
- Toggle switch to switch between time formats

### Getting Selected Time Values
Access the selected time components:
```powerpoint
// Get selected hour
drpHour.Selected.Value

// Get selected minute  
dprMinute.Selected.Value

// Get AM/PM (if not military time)
drpAMPM.Selected.Value

// Check if military time is enabled
showMilitary
```

### Setting Default Time
Customize the default selected times by modifying the `DefaultSelectedItems` properties:
```powerpoint
// Set default hour (12-hour format)
drpHour.DefaultSelectedItems = ["06"]

// Set default minute
dprMinute.DefaultSelectedItems = ["30"]

// Set default AM/PM
drpAMPM.DefaultSelectedItems = ["PM"]
```

### Switching Time Formats
The component includes a toggle to switch between formats:
- **12-hour format**: Shows hours 01-12 with AM/PM dropdown
- **24-hour format**: Shows hours 00-23 without AM/PM dropdown

Toggle military time programmatically:
```powerpoint
Set(showMilitary, true)   // Enable 24-hour format
Set(showMilitary, false)  // Enable 12-hour format
```

## Context Variables

- `showMilitary` (Boolean): Controls whether to display 24-hour or 12-hour time format

## Customization

### Label Text
Modify the component label:
```powerpoint
txtTimePickerLabel.Text = "Select Time"
```

### Required Field Indicator
Hide or show the required asterisk:
```powerpoint
txtRequiredStar.Visible = false  // Hide asterisk
txtRequiredStar.Text = ""        // Remove asterisk text
```

### Styling
- **Container dimensions**: Adjust `ctrTimePicker` Width and Height properties
- **Label styling**: Modify `txtTimePickerLabel` font weight and alignment
- **Dropdown styling**: Customize dropdown appearance through their properties
- **Spacing**: Adjust `LayoutGap` and padding properties in containers

### Validation
Add validation by setting the `ValidationState` property on dropdowns:
```powerpoint
// Example: Require hour selection
drpHour.ValidationState = If(IsBlank(drpHour.Selected), "Invalid", "Valid")
```

### Accessibility
The component includes accessibility features:
- `AccessibleLabel` properties on hour and minute dropdowns
- Proper semantic structure with containers and labels
- Keyboard navigation support through dropdown controls

## Component Structure

- **ctrTimePicker**: Main container with vertical auto-layout
  - **ctrTimePickerLabel**: Horizontal container for label and required indicator
    - **txtRequiredStar**: Required field asterisk
    - **txtTimePickerLabel**: Component label text
  - **ctrHrMinPickers**: Horizontal container for time selection controls
    - **drpHour**: Hour selection dropdown
    - **colonSeparator**: Colon separator between hour and minute
    - **dprMinute**: Minute selection dropdown
    - **ampmSeparator**: Separator between minute and AM/PM
    - **drpAMPM**: AM/PM selection dropdown (hidden in military time)
- **tglShowMilitary**: Toggle switch for time format selection

## Tips

- The component automatically adjusts dropdown widths based on the time format
- Use the `DisplayMode` property to make the entire component read-only
- Consider adding validation to ensure both hour and minute are selected
- The military time toggle can be hidden if only one format is needed
- Component width of 320px provides optimal layout for most scenarios
