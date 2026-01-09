<h1 align="center">PowerToys: Advanced Windows Productivity Suite</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**PowerToys** is a powerful, open-source suite of utilities from Microsoft that supercharges Windows productivity. With Winfig Dots, PowerToys is pre-configured for advanced workflows, custom keybindings, and enhanced system tools—making Windows 11 faster, smarter, and more customizable than ever.

---

## Features

- **Custom Keybindings:** Advanced, ergonomic shortcuts for every tool.
- **Command Not Found Handler:** Instantly suggests fixes for mistyped commands.
- **Environment Variables Manager:** Edit and manage environment variables with a GUI.
- **Hosts File Editor:** Safely edit your system hosts file.
- **Registry Preview:** View and edit Windows Registry files with syntax highlighting.
- **File Explorer Add-ons:** Preview SVG, Markdown, PDF, and more directly in Explorer.
- **File Locksmith:** See which processes are locking a file.
- **Image Resizer:** Batch resize images from the context menu.
- **New+ Templates:** Custom templates symlinked for quick file creation.
- **Peek:** Quick file preview with <kbd>Space</kbd>.
- **PowerRename:** Advanced batch renaming tool.
- **Find My Mouse:** Shake mouse to locate cursor instantly.
- **Always On Top:** Pin any window with <kbd>Win</kbd> + <kbd>Ctrl</kbd> + <kbd>T</kbd>.
- **Workspaces:** Organize windows with <kbd>Win</kbd> + <kbd>/</kbd>.
- **ZoomIt:** Advanced screen zoom, draw, and timer tools.
- **Text Extractor:** OCR any screen region with <kbd>Win</kbd> + <kbd>T</kbd>.
- **Shortcut Guide:** View all shortcuts with <kbd>Alt</kbd> + <kbd>F1</kbd>.
- **PowerToys Run:** Fast launcher with <kbd>Win</kbd> + <kbd>Space</kbd> (Calculator, Programs, URLs, etc.).
- **Color Picker:** Pick colors anywhere with <kbd>Win</kbd> + <kbd>C</kbd>.
- **Awake:** Keep your PC awake on demand.
- **Advanced Paste:** Smart clipboard and paste enhancements.

---
## Requirements

- [x] [PowerToys](https://docs.microsoft.com/powertoys/) installed on Windows 11
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) installed for dotfile management
- [x] Administrator privileges for certain configurations
- [x] Internet access for downloading dependencies
- [x] [Nerd Fonts (Hack Nerd Font)](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/Hack.zip) for enhanced terminal and UI appearance

!!! tip "Quick Install"
    - **PowerToys:**
        `winget install --id Microsoft.PowerToys -e`
    - **Git:**
        `winget install --id Git.Git -e`
    - **PowerShell 7 (optional, recommended):**
        `winget install --id Microsoft.Powershell -e`
    - **Hack Nerd Fonts:**
        Download from [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/Hack.zip) and install your favorite patched font.

---

## Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Powertoys/setup.ps1 | Invoke-Expression
    ```

    !!! success "Why Web Install?"
        - Always gets the latest version
        - No manual download required
        - Automatic script verification
    ![Web Install Demo](../images/19.png)

=== "Local Install"

    **Download and run manually** for offline environments:

    ```powershell title="1. Set Execution Policy"
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

    ```powershell title="2. Download Script"
    # Download from GitHub
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Powertoys/setup.ps1" -OutFile "setup.ps1"
    ```

    ```powershell title="3. Unblock and Run"
    Unblock-File -Path .\setup.ps1
    .\setup.ps1
    ```

    !!! warning "Note"
        - Ensure you have the latest script version
        - Manual updates required for new releases
        - Verify script integrity before running
    ![Local Install Demo](../images/20.png)

---

## Post-Installation

1. **Restart PowerToys** to apply new settings.
2. **Test Keybindings:** Try enabled shortcuts (see below) to confirm functionality.
3. **Review Modules:** Open PowerToys Settings to enable/disable or tweak modules.
4. **Customize Templates:** Add files to your Templates folder for New+.
5. **Backup:** Export your settings for future use or sharing.

!!! info "Need Help?"
    - Visit the [PowerToys documentation](https://docs.microsoft.com/powertoys/) for advanced features.
    - [Open an issue](https://github.com/Get-Winfig/winfig-docs/issues) if you encounter problems with the Winfig setup.

---


## Tips & Usage Notes

- **Custom Keymaps:** Winfig PowerToys dotfiles use advanced, ergonomic shortcuts for every module.
- **Templates:** Add your own templates to `%USERPROFILE%\.Dotfiles\winfig-dots\Powertoys` (symlinked to `C:\Windows\Resources\Templates`).
- **Safe Customization:** All configs are modular—feel free to tweak or extend as you like!
- **Minimal Bloat:** Only essential modules and plugins are enabled for speed and clarity.

---

## Keymaps & Enabled Modules

### Advance

- **Command Not Found:**
- **Environment Variables:**
- **Hosts File Editor:**
- **Registry Preview:**

### File Manager

- **File Explorer add-ons:**
- **File Locksmith:**
- **Image Resizer:**
- **New+:**
    Templates: `%USERPROFILE%\.Dotfiles\winfig-dots\Powertoys` → `C:\Windows\Resources\Templates`

- **Peek:**
    Keymap: <kbd>Space</kbd>

- **PowerRename:**

### Input / Output

- **Mouse utilities:**
  Only **Find My Mouse** is enabled (Shake mouse to view cursor position)

### Windowing & Layouts

- **Always On Top:**
    Shortcut: <kbd>Win</kbd> + <kbd>Ctrl</kbd> + <kbd>T</kbd>

- **Workspaces:**
    Shortcut: <kbd>Win</kbd> + <kbd>/</kbd>

- **Always On Top (Alt):**
    Shortcut: <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>T</kbd>

### System Tools

- **ZoomIt:**
    - <kbd>Ctrl</kbd> + <kbd>1</kbd>: Zoom
    - <kbd>Ctrl</kbd> + <kbd>4</kbd>: Live Zoom
    - <kbd>Ctrl</kbd> + <kbd>2</kbd>: Draw Without Zoom
    - <kbd>Ctrl</kbd> + <kbd>3</kbd>: Start Break Timer (1 min)
    - <kbd>Ctrl</kbd> + <kbd>5</kbd>: Record Video
    - <kbd>Ctrl</kbd> + <kbd>6</kbd>: Copy Region

- **Text Extractor:**
    Shortcut: <kbd>Win</kbd> + <kbd>T</kbd>

- **Shortcut Guide:**
    Shortcut: <kbd>Alt</kbd> + <kbd>F1</kbd>

- **PowerToys Run:**
    Shortcut: <kbd>Win</kbd> + <kbd>Space</kbd>
    Enabled Plugins:

    1. Calculator
    2. PowerToys
    3. Programs
    4. URL Handler

- **Color Picker:**
    Shortcut: <kbd>Win</kbd> + <kbd>C</kbd>

- **Awake:**
- **Advanced Paste:**

---

## Frequently Asked Questions (FAQ)

??? question "Can I use my own PowerToys settings?"
    Yes! Back up your current settings before applying Winfig dotfiles. You can always restore or merge your preferences later.

??? question "Is this safe to use?"
    All scripts and configs are open source. Review them on [GitHub](https://github.com/Get-Winfig/winfig-dots) before running.

??? question "How do I update my PowerToys dotfiles?"
    Simply re-run the web install command to fetch and apply the latest version.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Hotkeys not working             | Check for conflicts with other apps or reassign in PowerToys Settings.    |
| Module not enabled              | Open PowerToys Settings and enable the desired module.                    |
| Settings not applied            | Ensure you replaced the correct settings file and restarted PowerToys.    |
| Script errors during install    | Run PowerShell as Administrator and check execution policy.               |

If your issue isn’t listed, check the [PowerToys FAQ](https://docs.microsoft.com/powertoys/) or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
