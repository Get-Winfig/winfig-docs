<h1 align="center">Winfig Customization: Windows Themes, Fonts & Cursors</h1>

![Winfig Banner](images/Banner.png)

<div align="center">
  <strong>Personalize your Windows experience with beautiful fonts, cursor themes, and visual customizations</strong>
</div>

---

## Overview

**Winfig Customization** provides automated scripts to install and configure custom fonts, cursor themes, and visual enhancements for Windows. Transform your desktop with beautiful Nerd Fonts, modern cursor themes, and seamless integration with your Winfig Dots ecosystem.

---

## Features

- **Automated Font Install**: One-command install for Hack and JetBrainsMono Nerd Fonts.
- **Cursor Theme Manager**:  Interactive menu for selecting and installing cursor themes.
- **Windhawk Mods** (UI tweaks, taskbar enhancements, system modifications)

---

## Why Use Winfig Customization?

- **Save time** with automated, one-click installation
- **Beautiful fonts** optimized for terminals and code editors
- **Modern cursor themes** for a polished desktop experience
- **Powerful Windhawk mods** for deep Windows UI customization
- **Consistent theming** across your entire Winfig ecosystem
- **Easy rollback** and uninstall options
- **Portable & reproducible** setups for fresh installs or VMs

---

## Nerd Fonts Setup

### Requirements

- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) for cloning the customization repository
- [x] Administrator privileges for font installation
- [x] Internet access for downloading dependencies

### Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-customization/refs/heads/main/Fonts/setup.ps1 | Invoke-Expression
    ```

    !!! success "Why Web Install?"
        - Always gets the latest version
        - No manual download required
        - Automatic script verification
        - Clones repo and installs fonts in one step

=== "Local Install"

    **Download and run manually** for offline environments:

    ```powershell title="1. Set Execution Policy"
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

    ```powershell title="2. Download Script"
    # Download from GitHub
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/refs/heads/main/Fonts/setup.ps1" -OutFile "setup.ps1"
    ```

    ```powershell title="3. Unblock and Run"
    Unblock-File -Path .\setup.ps1
    .\setup.ps1
    ```

    !!! warning "Note"
        - Ensure you have the latest script version
        - Manual updates required for new releases
        - Verify script integrity before running

### Post-Installation

1. **Restart Windows** to apply font changes system-wide
2. **Refresh font cache** (automatically done by the script)
3. **Select your new font** in:
    - Windows Terminal: Settings → Appearance → Font face
    - VS Code: Settings → Font Family
    - Your favorite terminal or code editor

> **Tip:** Use `JetBrainsMono Nerd Font` or `Hack Nerd Font` for the best icon support in Starship, Oh My Posh, and other terminal prompts.

---

## Cursor Themes Setup

### Requirements

- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) for cloning the customization repository
- [x] Administrator privileges for cursor installation
- [x] Internet access for downloading dependencies

### Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-customization/refs/heads/main/Cursors/setup.ps1 | Invoke-Expression
    ```

    !!! success "Why Web Install?"
        - Always gets the latest version
        - No manual download required
        - Automatic script verification
        - Interactive menu for theme selection

=== "Local Install"

    **Download and run manually** for offline environments:

    ```powershell title="1. Set Execution Policy"
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

    ```powershell title="2. Download Script"
    # Download from GitHub
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/refs/heads/main/Cursors/setup.ps1" -OutFile "setup.ps1"
    ```

    ```powershell title="3. Unblock and Run"
    Unblock-File -Path .\setup.ps1
    .\setup.ps1
    ```

    !!! warning "Note"
        - Ensure you have the latest script version
        - Manual updates required for new releases
        - Verify script integrity before running

### Available Cursor Themes

The script provides an interactive menu to choose from multiple modern cursor themes:

=== "Sunity Cursors"

    | Dark Variant | Light Variant |
    |:------------:|:-------------:|
    | ![Sunity Dark Theme](./images/64.png) | ![Sunity Light Theme](./images/65.png) |
    | Perfect for dark mode enthusiasts | Ideal for light interface users |

    !!! info "Features"
        - Smooth animations
        - High-DPI support
        - Multiple pointer styles
        - Available in Light and Dark variants

=== "Win 11 Concept"

    <div align="center">
        <img src="./images/66.jpg" alt="Win 11 Concept Theme" width="600">
        <p><em>Available in both Dark and Light variants</em></p>
    </div>

    !!! info "Features"
        - Modern Windows 11 aesthetic
        - Consistent with system design language
        - Optimized for 4K displays
        - Available in Light and Dark variants

### Post-Installation Steps

#### 1. Manual Installation (Required)

The script will open the cursor folder and display instructions. Follow these steps:

1. In the opened folder, **right-click** on `Install.inf`
2. Select **"Install"** from the context menu
3. Follow any prompts to complete installation

> **Note:** Windows requires manual installation for security reasons. The script guides you through this process.

#### 2. Apply Cursor Theme

1. Go to **Settings** → **Personalization** → **Themes** → **Mouse cursor**
2. Select your new cursor theme from the list
3. Click **Apply**

#### 3. Restart (Recommended)

For best results, **restart Windows** after applying the cursor theme.

---

## Windhawk Mods Setup

### What is Windhawk?

[Windhawk](https://windhawk.net/) is a powerful customization platform for Windows that allows you to modify system UI and behavior using community-created mods. Winfig Customization provides pre-configured settings for 15 carefully selected mods to enhance your Windows experience.

### Requirements

- [x] [Windhawk](https://windhawk.net/) installed on Windows 11
- [x] Internet access for downloading mods
- [x] Administrator privileges (recommended)

### Supported Windhawk Mods

Below are all 15 Winfig-optimized mods available with pre-configured settings:

| Mod Name | Description |
|----------|-------------|
| **Taskbar Dock Animation** | Smooth dock-style animations for taskbar icons |
| **Taskbar Icon Size** | Customize taskbar icon sizes for better visibility |
| **Taskbar Tray System Icon Tweaks** | Fine-tune system tray icon spacing and behavior |
| **Windows 11 Taskbar Styler** | Advanced taskbar appearance customization |
| **Better File Sizes in Explorer Details** | Show more readable file sizes in Explorer |
| **Disk Pie Chart** | Visual disk space representation in Explorer |
| **Windows 11 File Explorer Styler** | Customize File Explorer colors, spacing, and UI |
| **Extension Change No Warning** | Disable file extension change warnings |
| **Modernize Folder Picker Dialog** | Update old-style folder picker to modern UI |
| **Translucent Windows** | Enable transparency and blur effects on windows |
| **Icon Resource Redirect** | Replace system icons with custom alternatives |
| **Disable Virtual Desktop Transition** | Remove virtual desktop switching animations |
| **Windows 11 Start Menu Styler** | Customize Start Menu appearance and layout |
| **Windows 11 Notification Center Styler** | Style notification center colors and design |
| **Notifications Placement** | Control where notifications appear on screen |

### Installation Instructions

Follow these steps to install and configure any Windhawk mod with Winfig settings:

#### Step 1: Install Windhawk

If you haven't installed Windhawk yet:

1. Download from [windhawk.net](https://windhawk.net/)
2. Run the installer and follow the setup wizard
3. Launch Windhawk from the Start menu or system tray

#### Step 2: Install a Mod

1. Open **Windhawk**
2. Go to the **Explore** tab
3. Use the search bar to find the mod you want (e.g., "Taskbar Dock Animation")
4. Click **Install** and wait for installation to complete
5. The mod will appear in the **Installed Mods** tab

#### Step 3: Import Winfig Configuration

1. In Windhawk, click on the installed mod to open its **Details** page
2. Navigate to the **Advanced** section
3. Copy the configuration JSON from the mod's config section below
4. Paste the copied config into the **Mod settings** field
5. Click **Save** to apply the configuration

#### Step 4: Apply Changes

Most mods require restarting Windows Explorer:

```powershell title="Restart Windows Explorer"
Stop-Process -Name explorer -Force
```

Or use Windhawk's built-in restart:
- Right-click Windhawk tray icon → **Restart Explorer**

!!! success "Done!"
    Your mod is now installed and configured with Winfig's optimized settings!

### Mod Configurations

Below are the pre-configured settings for each mod. Click to download or view the config directly from GitHub.

#### Taskbar Dock Animation

Adds smooth, macOS-style dock animations when hovering over taskbar icons.

```json title="taskbar-dock-animation.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/taskbar-dock-animation.json"
```

#### Taskbar Icon Size

Sets taskbar icons to 32px for optimal balance between visibility and space efficiency.

```json title="taskbar-icon-size.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/taskbar-icon-size.json"
```

#### Taskbar Tray System Icon Tweaks

Reduces system tray clutter with optimized spacing and hidden redundant icons.

```json title="taskbar-tray-system-icon-tweaks.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/taskbar-tray-system-icon-tweaks.json"
```

#### Windows 11 Taskbar Styler

Applies beautiful Catppuccin theming to your taskbar with transparency and modern styling.

```json title="windows-11-taskbar-styler.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/windows-11-taskbar-styler.json"
```

#### Better File Sizes in Explorer Details

Displays file sizes in a more readable format (e.g., "1.5 GB" instead of "1,536 MB").

```json title="Better-file-sizes-in-Explorer-details.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/Better-file-sizes-in-Explorer-details.json"
```

#### Disk Pie Chart

Adds visual pie charts to "This PC" view showing disk space usage at a glance.

```json title="disk-pie-chart.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/disk-pie-chart.json"
```

#### Windows 11 File Explorer Styler

Transforms File Explorer with beautiful Catppuccin theming and improved UI.

```json title="windows-11-file-explorer-styler.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/windows-11-file-explorer-styler.json"
```

#### Extension Change No Warning

Removes the annoying warning when changing file extensions (for power users).

```json title="extension-change-no-warning.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/extension-change-no-warning.json"
```

---

#### Modernize Folder Picker Dialog

Replaces old-style folder picker dialogs with modern Windows 11 UI.

```json title="modernize-folder-picker-dialog.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/modernize-folder-picker-dialog.json"
```

#### Translucent Windows

Adds beautiful transparency and blur effects to windows for a modern, macOS-like aesthetic.

```json title="translucent-windows.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/translucent-windows.json"
```

#### Icon Resource Redirect

Replaces default Windows system icons with custom alternatives.

```json title="icon-resource-redirect.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/icon-resource-redirect.json"
```

#### Disable Virtual Desktop Transition

Removes the sliding animation when switching virtual desktops for instant transitions.

```json title="disable-virtual-desktop-transition.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/disable-virtual-desktop-transition.json"
```

#### Windows 11 Start Menu Styler

Customizes Start Menu with beautiful theming and improved layout.

```json title="windows-11-start-menu-styler.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/windows-11-start-menu-styler.json"
```

#### Windows 11 Notification Center Styler

Styles notification center to match your Catppuccin theme.

```json title="windows-11-notification-center-styler.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/windows-11-notification-center-styler.json"
```

#### Notifications Placement

Controls notification placement on screen (great for multi-monitor setups).

```json title="notifications-placement.json"
--8<-- "https://raw.githubusercontent.com/Get-Winfig/winfig-customization/main/Windhawk/notifications-placement.json"
```

---

## Frequently Asked Questions (FAQ)

??? question "Do I need administrator privileges?"
    Yes, both font and cursor installation require administrator rights for system-wide installation.

??? question "Will this overwrite my existing fonts or cursors?"
    Fonts are added alongside existing ones. Cursor themes can be switched at any time without removing old ones.

??? question "Can I uninstall these customizations?"
    Yes. Fonts can be removed from `C:\Windows\Fonts`, and cursor themes can be uninstalled via Settings → Mouse cursor settings.

??? question "Do these work on Windows 10?"
    Yes, both scripts work on Windows 10 and Windows 11.

??? question "How do I update to the latest fonts/cursors?"
    Re-run the installation scripts. They will automatically update the Winfig Customization repository.

??? question "Why do I need to manually install cursors?"
    Windows security policies require manual installation of cursor themes via right-click → Install.

??? question "Can I use these fonts in other applications?"
    Yes! Once installed, Nerd Fonts work in any application that supports custom fonts (VS Code, terminals, browsers, etc.).

??? question "Are these scripts safe?"
    All scripts are open source and can be reviewed on the [Winfig GitHub repository](https://github.com/Get-Winfig/winfig-customization).

---

## Troubleshooting Guide

??? warning "Fonts not appearing after installation"
    - **Restart Windows** to refresh the font cache
    - **Check font installation**: Open `C:\Windows\Fonts` and verify Nerd Fonts are present
    - **Clear font cache manually**:
      ```powershell
      Stop-Service -Name "FontCache"
      Remove-Item -Path "$env:LOCALAPPDATA\Microsoft\Windows\Caches\*" -Recurse -Force
      Start-Service -Name "FontCache"
      ```
    - **Reinstall fonts**: Run the script again with elevated privileges

??? warning "Cursor theme not applying"
    - **Restart Windows** after installing the cursor theme
    - **Manually apply**: Go to Settings → Personalization → Themes → Mouse cursor
    - **Check installation**: Verify the cursor files are in `C:\Windows\Cursors`
    - **Use Control Panel**: Search for "Change mouse pointer" and select your theme from the list

??? warning "Script execution blocked or errors"
    - **Check execution policy**:
      ```powershell
      Get-ExecutionPolicy
      Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
      ```
    - **Run as Administrator**: Right-click PowerShell → Run as Administrator
    - **Unblock downloaded files**:
      ```powershell
      Unblock-File -Path .\setup.ps1
      ```
    - **Check antivirus**: Temporarily disable antivirus if it's blocking script execution

??? warning "Windhawk mods not working or crashing"
    - **Update Windhawk**: Download the latest version from [windhawk.net](https://windhawk.net/)
    - **Restart Windows Explorer**: `Stop-Process -Name explorer -Force`
    - **Disable conflicting mods**: Some mods may conflict with each other (e.g., multiple taskbar mods)
    - **Check mod compatibility**: Ensure the mod supports your Windows version
    - **Reinstall the mod**: Uninstall and reinstall the problematic mod
    - **Clear Windhawk cache**: Settings → Advanced → Clear cache

??? warning "Repository clone or download fails"
    - **Check internet connection**: Ensure stable internet access
    - **Verify Git installation**: `git --version`
    - **Use HTTPS instead of SSH**: Clone with HTTPS URL if SSH fails
    - **Check GitHub status**: Visit [githubstatus.com](https://githubstatus.com)
    - **Manual download**: Download ZIP from GitHub and extract manually

??? warning "Performance issues after installing mods"
    - **Disable resource-heavy mods**: Such as Translucent Windows or animations
    - **Reduce transparency levels**: Lower opacity settings in mod configs
    - **Check system resources**: Open Task Manager to monitor CPU/RAM usage
    - **Disable unnecessary mods**: Keep only essential mods enabled
    - **Update graphics drivers**: Ensure GPU drivers are up to date

??? warning "Nerd Font icons not displaying correctly"
    - **Select the correct font variant**: Use "Nerd Font" or "Nerd Font Mono" versions
    - **Check terminal/editor settings**: Ensure the font is properly selected
    - **Verify Unicode support**: Your application must support Unicode characters
    - **Update your terminal**: Use Windows Terminal, Alacritty, or other modern terminals
    - **Test with font preview**: Open `C:\Windows\Fonts` and preview the font

??? warning "Cursor animation or effects not working"
    - **Enable cursor shadow**: Settings → Mouse → Additional mouse options → Pointer Options → Enable pointer shadow
    - **Check display scaling**: High DPI settings may affect cursor rendering
    - **Use native resolution**: Cursor themes work best at native display resolution
    - **Disable hardware acceleration**: In some apps if cursor appears glitchy

??? warning "Config import fails in Windhawk"
    - **Verify JSON syntax**: Ensure the config file is valid JSON
    - **Copy entire content**: Select all and copy the complete JSON object
    - **Use raw GitHub link**: Copy from raw.githubusercontent.com URLs
    - **Check mod version**: Ensure config matches your mod version
    - **Manually edit settings**: Input values directly in Windhawk settings UI

??? warning "Need more help?"
    - Visit the [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-customization/issues) page
    - Check [Winfig Discussions](https://github.com/Get-Winfig/winfig-customization/discussions) for community help
    - Review the full documentation at [winfig-docs](https://get-winfig.github.io/winfig-docs)
    - Open a new issue with detailed error logs and system information
