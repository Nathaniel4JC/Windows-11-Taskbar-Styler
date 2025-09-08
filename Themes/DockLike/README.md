# DockLike theme for Windows 11 Taskbar Styler

**Author**: [Amber](https://github.com/AmberWat)

![Screenshot of taskbar](screenshot.png)

## Notes

This theme is meant as a fairly vanilla implementation of a dock-like taskbar. It works great out of the box, but there are several tweaks that can be made.

### Suggested Windows settings

- Set taskbar alignment to center
- Hide the widgets button
- If you have another clock, for example from a Rainmeter skin or an application like ElevenClock, you can hide the taskbar clock in Windows date & time settings

### Left align the taskbar (tweak)

Do not use the Windows taskbar setting to left align. Instead, add the following control styles:

Target:
```
Taskbar.TaskbarFrame
```
Styles:
```
HorizontalAlignment=Left
Margin=0,0,250,0
```

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Style:
```
CornerRadius=0,8,0,0
```

### Make the taskbar float (tweak)

This gives it an appearance closer to the MacOS dock.

![Screenshot of floating taskbar](screenshot_floating.png)

1. Use the mod [Taskbar height and icon size](https://windhawk.net/mods/taskbar-icon-size) to increase the height of the taskbar by 4 (usually from 48 to 52). This compensates for the added spacing.

2. Add the following control styles:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Styles:
```
Margin=0,1,0,3
```
```
CornerRadius=8
```

Target:
```
Grid#SystemTrayFrameGrid
```
Style:
```
Margin=8,1,8,3
```

### Add a border (tweak)

1. Add the following control styles:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Styles:
```
BorderThickness=1
```
```
BorderBrush:=<SolidColorBrush Color="{ThemeResource SurfaceStrokeColorDefault}" />
```

Target:
```
Grid#SystemTrayFrameGrid
```
Styles:
```
BorderThickness=1
```
```
BorderBrush:=<SolidColorBrush Color="{ThemeResource SurfaceStrokeColorDefault}" />
```

2. If you haven't applied the floating taskbar tweak, add the following control style:

Target:
```
Taskbar.TaskbarFrame > Grid#RootGrid
```
Style:
```
Margin=0,0,0,-2
```

## Theme selection

The theme is integrated into the mod and can simply be selected from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Taskbar.TaskbarFrame",
  "controlStyles[0].styles[0]": "Width=Auto",
  "controlStyles[0].styles[1]": "HorizontalAlignment=Center",
  "controlStyles[0].styles[2]": "Margin=250,0,250,0",

  "controlStyles[1].target": "Taskbar.TaskbarFrame > Grid#RootGrid",
  "controlStyles[1].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeAltHighColor}\" TintOpacity=\"0.8\" FallbackColor=\"{ThemeResource SystemChromeLowColor}\" />",
  "controlStyles[1].styles[1]": "Padding=6,0,6,0",
  "controlStyles[1].styles[2]": "CornerRadius=8,8,0,0",
  "controlStyles[1].styles[3]": "BorderBrush:=<SolidColorBrush Color=\"{ThemeResource SurfaceStrokeColorDefault}\" />",

  "controlStyles[2].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[2].styles[0]": "Visibility=Collapsed",

  "controlStyles[3].target": "Rectangle#BackgroundStroke",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",

  "controlStyles[4].target": "Taskbar.AugmentedEntryPointButton#AugmentedEntryPointButton > Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel",
  "controlStyles[4].styles[0]": "Margin=0",

  "controlStyles[5].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[5].styles[0]": "Background:=<AcrylicBrush TintColor=\"{ThemeResource SystemChromeAltHighColor}\" TintOpacity=\"0.8\" FallbackColor=\"{ThemeResource SystemChromeLowColor}\" />",
  "controlStyles[5].styles[1]": "Margin=-4,-8,-4,-8",
  "controlStyles[5].styles[2]": "CornerRadius=10",
  "controlStyles[5].styles[3]": "BorderThickness=12,12,12,12",
  "controlStyles[5].styles[4]": "BackgroundSizing=InnerBorderEdge",

  "controlStyles[6].target": "SystemTray.ChevronIconView",
  "controlStyles[6].styles[0]": "Padding=0",

  "controlStyles[7].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[7].styles[0]": "Padding=0",

  "controlStyles[8].target": "SystemTray.OmniButton",
  "controlStyles[8].styles[0]": "Padding=0",

  "controlStyles[9].target": "SystemTray.CopilotIcon",
  "controlStyles[9].styles[0]": "Padding=0",

  "controlStyles[10].target": "SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > systemtray:IconView#SystemTrayIcon > Grid",
  "controlStyles[10].styles[0]": "Padding=4,0,4,0",

  "controlStyles[11].target": "SystemTray.IconView#SystemTrayIcon > Grid#ContainerGrid > ContentPresenter#ContentPresenter > Grid#ContentGrid > SystemTray.TextIconContent > Grid#ContainerGrid",
  "controlStyles[11].styles[0]": "Padding=0",

  "controlStyles[12].target": "SystemTray.StackListView#IconStack > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon",
  "controlStyles[12].styles[0]": "Padding=0",

  "controlStyles[13].target": "SystemTray.Stack#ShowDesktopStack",
  "controlStyles[13].styles[0]": "Margin=0,-4,-12,-4",

  "controlStyles[14].target": "Taskbar.Gripper#GripperControl",
  "controlStyles[14].styles[0]": "Width=Auto",
  "controlStyles[14].styles[1]": "MinWidth=24"
}
```
</details>
