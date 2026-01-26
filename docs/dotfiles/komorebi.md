

<h1 align="center">Komorebi: Advanced Tiling Window Management for Windows</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**Komorebi** is a fast, feature-rich tiling window manager for Windows, bringing advanced workspace, stacking, and automation features to your desktop. With Winfig Dots, Komorebi is pre-configured for beautiful borders, smooth animations, workspace rules, and seamless integration with whkd for ergonomic keyboard-driven workflows.

---

## Features

- True tiling window management on Windows
- Customizable workspaces with per-app rules
- Beautiful rounded borders and Catppuccin-inspired colors
- Smooth animations (144fps, cubic easing)
- Stack, monocle, and BSP layouts
- Keyboard-driven navigation and manipulation (via whkd)
- Transparency, floating, and monocle toggles
- Seamless integration with Winfig Dots ecosystem

---

## Requirements

- [x] [Komorebi](https://github.com/LGUG2Z/komorebi) v0.1.28+
- [x] [whkd](https://github.com/whkd/whkd) for hotkey handling
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for scripting
- [x] Windows 11 (recommended)
- [x] [Nerd Font](https://www.nerdfonts.com/) for icons and symbols
- [x] Administrator privileges for installation

!!! tip "Quick Install"
    - **Komorebi:**
      `winget install --id LGUG2Z.Komorebi -e`
    - **whkd:**
      `winget install --id LGUG2Z.whkd -e`
    - **Git:**
      `winget install --id Git.Git -e`
    - **PowerShell 7 (optional, recommended):**
      `winget install --id Microsoft.Powershell -e`
    - **Nerd Font:**
      Download and install from [Nerd Fonts](https://www.nerdfonts.com/font-downloads)

---

## Installation Methods

=== "Web Install (Recommended)"

  **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Bat/setup.ps1 | Invoke-Expression
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
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Bat/setup.ps1" -OutFile "setup.ps1"
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


## Hotkey Reference (whkdrc)

All navigation and manipulation is keyboard-driven via whkd. Below is a categorized table of all hotkeys from your real configuration:

### Focus Windows
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>H</kbd> | Focus left |
| <kbd>Alt</kbd>+<kbd>J</kbd> | Focus down |
| <kbd>Alt</kbd>+<kbd>K</kbd> | Focus up |
| <kbd>Alt</kbd>+<kbd>L</kbd> | Focus right |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>[</kbd> | Cycle focus previous |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>]</kbd> | Cycle focus next |

### Move Windows
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>H</kbd> | Move left |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>J</kbd> | Move down |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>K</kbd> | Move up |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>L</kbd> | Move right |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Enter</kbd> | Promote window |

### Stack Windows
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>Left</kbd> | Stack left |
| <kbd>Alt</kbd>+<kbd>Down</kbd> | Stack down |
| <kbd>Alt</kbd>+<kbd>Up</kbd> | Stack up |
| <kbd>Alt</kbd>+<kbd>Right</kbd> | Stack right |
| <kbd>Alt</kbd>+<kbd>;</kbd> | Unstack |
| <kbd>Alt</kbd>+<kbd>[</kbd> | Cycle stack previous |
| <kbd>Alt</kbd>+<kbd>]</kbd> | Cycle stack next |

### Resize
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>+</kbd> | Resize horizontal increase |
| <kbd>Alt</kbd>+<kbd>-</kbd> | Resize horizontal decrease |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>+</kbd> | Resize vertical increase |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>-</kbd> | Resize vertical decrease |

### Manipulate Windows
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>T</kbd> | Toggle float |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd> | Toggle monocle |

### Window Manager Options
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>R</kbd> | Retile |
| <kbd>Alt</kbd>+<kbd>P</kbd> | Toggle pause |

### Layouts
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>X</kbd> | Flip layout horizontal |
| <kbd>Alt</kbd>+<kbd>Y</kbd> | Flip layout vertical |

### Workspaces
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>1</kbd> | Focus workspace 1 |
| <kbd>Alt</kbd>+<kbd>2</kbd> | Focus workspace 2 |
| <kbd>Alt</kbd>+<kbd>3</kbd> | Focus workspace 3 |
| <kbd>Alt</kbd>+<kbd>4</kbd> | Focus workspace 4 |
| <kbd>Alt</kbd>+<kbd>5</kbd> | Focus workspace 5 |
| <kbd>Alt</kbd>+<kbd>6</kbd> | Focus workspace 6 |
| <kbd>Alt</kbd>+<kbd>7</kbd> | Focus workspace 7 |
| <kbd>Alt</kbd>+<kbd>8</kbd> | Focus workspace 8 |
| <kbd>Alt</kbd>+<kbd>9</kbd> | Focus workspace 9 |
| <kbd>Alt</kbd>+<kbd>0</kbd> | Focus workspace 10 |

### Move Windows Across Workspaces
| Hotkey | Action |
|--------|--------|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>1</kbd> | Move to workspace 1 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>2</kbd> | Move to workspace 2 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>3</kbd> | Move to workspace 3 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>4</kbd> | Move to workspace 4 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>5</kbd> | Move to workspace 5 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>6</kbd> | Move to workspace 6 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>7</kbd> | Move to workspace 7 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>8</kbd> | Move to workspace 8 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>9</kbd> | Move to workspace 9 |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>0</kbd> | Move to workspace 10 |

---

## Customization Tips

- Edit `komorebi.json` to change border colors, animation, or workspace rules
- Edit `whkdrc` to remap hotkeys or add new commands
- Use Nerd Fonts for best stackbar appearance
- Combine with AutoHotkey for even more automation

---

## Frequently Asked Questions (FAQ)

??? question "How do I add or change hotkeys?"
    Edit your `whkdrc` file in any text editor. See the [whkd documentation](https://github.com/whkd/whkd) for syntax help.

??? question "How do I change workspace rules or layouts?"
    Edit `komorebi.json` and reload Komorebi. You can assign apps to workspaces and set layouts per workspace.

??? question "How do I make Komorebi/whkd run at startup?"
    Place shortcuts to both in the Windows Startup folder (`shell:startup`).

??? question "Can I use Komorebi with other automation tools?"
    Yes! Komorebi and whkd are designed to work alongside AutoHotkey, Winfig Dots, and other automation tools.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Komorebi not tiling windows    | Ensure Komorebi is running and config is valid. Check logs for errors.    |
| Hotkey not working             | Make sure whkd is running and `whkdrc` is correct.                       |
| Borders/colors not applied     | Check `komorebi.json` for color codes and border settings.                |
| Workspace rules not working    | Ensure app IDs are correct and Komorebi is reloaded after changes.        |
| Transparency not working       | Make sure transparency is enabled and supported by your system.           |

If your issue isn’t listed, check the [Komorebi documentation](https://github.com/LGUG2Z/komorebi), [whkd documentation](https://github.com/whkd/whkd), or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
