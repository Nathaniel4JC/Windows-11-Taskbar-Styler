# RosePine theme for Windows 11 Taskbar Styler

This theme was originally [shared on
Reddit](https://www.reddit.com/r/desktops/comments/1e0o08e/windows_11_rose_pine_been_messing_with_windhawk_a/).

**Author**: [asev](https://github.com/lunar-os)

![Screenshot](screenshot.png)

## Notes

* This theme is intended to be used with the following mods and settings.
  Install each mod, go to the "Advanced" tab, copy the settings to the text box
  under "Mod settings" and click "Save".
  * [Taskbar height and icon size](https://windhawk.net/mods/taskbar-icon-size):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20height%20and%20icon%20size).
  * [Taskbar Clock
    Customization](https://windhawk.net/mods/taskbar-clock-customization):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20Clock%20Customization).
  * [Taskbar Labels for Windows 11](https://windhawk.net/mods/taskbar-labels):
    [Settings](https://github.com/lunar-os/windowsdesktop/blob/main/WindhawkConfigs/Taskbar%20Labels).
* The theme is based off of [RosePine Theme](https://rosepinetheme.com/).
* It removes the start button and the network icon. If you need these, add them
  using the
  [guide](https://github.com/ramensoftware/windows-11-taskbar-styling-guide).
* Font used is [JetBrainsMono Nerd
  Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/JetBrainsMono.zip).

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
  "controlStyles[0].target": "Taskbar.TaskListButton",
  "controlStyles[0].styles[0]": "CornerRadius=3",
  "controlStyles[1].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[1].styles[0]": "FontSize=16",
  "controlStyles[2].target": "SystemTray.NotifyIconView#NotifyItemIcon",
  "controlStyles[2].styles[0]": "MinWidth=25",
  "controlStyles[3].target": "SystemTray.OmniButton#ControlCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter[1] > SystemTray.IconView > Grid > Grid",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[4].target": "SystemTray.TextIconContent > Grid#ContainerGrid",
  "controlStyles[4].styles[0]": "Padding=2",
  "controlStyles[5].target": "SystemTray.ChevronIconView",
  "controlStyles[5].styles[0]": "MinWidth=27",
  "controlStyles[6].target": "SystemTray.OmniButton#NotificationCenterButton > Grid > ContentPresenter > ItemsPresenter > StackPanel > ContentPresenter > SystemTray.IconView#SystemTrayIcon > Grid > Grid > SystemTray.TextIconContent",
  "controlStyles[6].styles[0]": "Visibility=Collapsed",
  "controlStyles[7].target": "Taskbar.TaskListLabeledButtonPanel > Border#BackgroundElement",
  "controlStyles[7].styles[0]": "Background:=#302d47",
  "controlStyles[8].target": "Grid#SystemTrayFrameGrid",
  "controlStyles[8].styles[0]": "Background:=#302d47",
  "controlStyles[8].styles[1]": "CornerRadius=6",
  "controlStyles[8].styles[2]": "Margin=0,5,4,4",
  "controlStyles[8].styles[3]": "Padding=3,0,-8,0",
  "controlStyles[7].styles[1]": "CornerRadius=6",
  "controlStyles[9].target": "Taskbar.TaskListLabeledButtonPanel@CommonStates > Rectangle#RunningIndicator",
  "controlStyles[9].styles[0]": "Height=27",
  "controlStyles[9].styles[1]": "RadiusX=5",
  "controlStyles[9].styles[2]": "RadiusY=5",
  "controlStyles[9].styles[3]": "StrokeThickness=2",
  "controlStyles[9].styles[4]": "Stroke@InactivePointerOver=#ebbcba",
  "controlStyles[9].styles[5]": "Stroke@InactivePressed=#ebbcba",
  "controlStyles[9].styles[6]": "Stroke@ActiveNormal=#ebbcba",
  "controlStyles[9].styles[7]": "Stroke@ActivePointerOver=#ebbcba",
  "controlStyles[9].styles[8]": "Stroke@ActivePressed=#ebbcba",
  "controlStyles[9].styles[9]": "Fill=Transparent",
  "controlStyles[9].styles[10]": "Width=37",
  "controlStyles[9].styles[11]": "VerticalAlignment=1",
  "controlStyles[9].styles[12]": "Canvas.ZIndex=1",
  "controlStyles[10].target": "SystemTray.ImageIconContent > Grid#ContainerGrid > Image",
  "controlStyles[10].styles[0]": "Width=13",
  "controlStyles[11].target": "SystemTray.TextIconContent > Grid#ContainerGrid > SystemTray.AdaptiveTextBlock#Base > TextBlock#InnerTextBlock",
  "controlStyles[11].styles[0]": "FontSize=14",
  "controlStyles[12].target": "TextBlock#LabelControl",
  "controlStyles[12].styles[0]": "FontFamily=JetBrainsMono NF",
  "controlStyles[12].styles[2]": "Padding=2,0,8,0",
  "controlStyles[13].target": "Taskbar.ExperienceToggleButton#LaunchListButton[AutomationProperties.AutomationId=StartButton]",
  "controlStyles[13].styles[0]": "Visibility=Collapsed",
  "controlStyles[12].styles[1]": "Foreground=#e0def4",
  "controlStyles[14].target": "Windows.UI.Xaml.Controls.TextBlock#InnerTextBlock[Text=]",
  "controlStyles[14].styles[0]": "Text=",
  "controlStyles[15].target": "Taskbar.TaskbarFrame > Grid#RootGrid > Taskbar.TaskbarBackground > Grid > Rectangle#BackgroundFill",
  "controlStyles[15].styles[0]": "Fill=Transparent",
  "controlStyles[16].target": "Taskbar.TaskbarBackground#HoverFlyoutBackgroundControl > Grid > Rectangle#BackgroundFill",
  "controlStyles[16].styles[0]": "Fill=#302d47",
  "controlStyles[17].target": "Rectangle#BackgroundStroke",
  "controlStyles[17].styles[0]": "Fill=Transparent",
  "controlStyles[18].target": "Taskbar.TaskListButtonPanel#ExperienceToggleButtonRootPanel > Border#BackgroundElement",
  "controlStyles[18].styles[0]": "Background=#302d47",
  "controlStyles[19].target": "TextBlock#DateInnerTextBlock",
  "controlStyles[19].styles[0]": "Margin=0,0,0,-2",
  "controlStyles[20].target": "Grid#OverflowRootGrid > Border",
  "controlStyles[20].styles[0]": "Background=#302d47"
}
```
</details>
