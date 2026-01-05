<h1 align="center">Starship: The Catppuccin-Powered Prompt for Any Shell</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**Starship** is a blazing-fast, highly customizable prompt for any shell—PowerShell, Bash, Zsh, and more. It brings beautiful icons, contextual info, and a Catppuccin Mocha palette to your terminal, making every session productive and visually stunning. With Winfig Dots, Starship is pre-configured for Windows with a modern, icon-rich, and language-aware prompt.

---

## Features

- **Catppuccin Mocha Palette:** Gorgeous, modern colors for every segment and symbol.
- **Multi-Language Support:** Shows version and context for Node.js, Python, Rust, Go, Java, PHP, C, Lua, and more.
- **Powerful Git Integration:** Branch, status, and icons for every repo state.
- **OS & Directory Icons:** Custom icons for OS, folders, and common directories.
- **Segmented Powerline Style:** Beautiful, multi-color segments with Unicode separators.
- **Fast & Cross-Shell:** Works with PowerShell, Bash, Zsh, and more.
- **Customizable Prompt:** Easily tweak format, palette, and modules.

---

## Requirements

- [x] [Starship](https://starship.rs/) installed on Windows 11
- [x] [Nerd Font](https://www.nerdfonts.com/) for icons and symbols
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) or any modern shell
- [x] [Git](https://git-scm.com/download/win) for Git integration
- [x] Administrator privileges for certain configurations
- [x] Internet access for downloading dependencies

!!! tip "Quick Install"
    - **Starship:**
      `winget install --id Starship.Starship -e`
    - **Nerd Font:**
      Download and install from [Nerd Fonts](https://www.nerdfonts.com/font-downloads)
    - **PowerShell 7 (optional, recommended):**
      `winget install --id Microsoft.Powershell -e`

---

## Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Starship/setup.ps1 | Invoke-Expression
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
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Starship/setup.ps1" -OutFile "setup.ps1"
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


## Configuration Highlights

- **Catppuccin Mocha Palette:**
  All segments use the Catppuccin Mocha color palette for a cohesive, modern look.
- **Powerline Segments:**
  Unicode separators and multi-color backgrounds for each module.
- **OS & Directory Icons:**
  Custom icons for Windows, Linux, macOS, and common folders.
- **Language Modules:**
  Shows version and icon for Node.js, Python, Rust, Go, Java, PHP, C, Lua, and more.
- **Git Branch & Status:**
  Beautiful icons and color-coded status for every repo state.
- **Time, Kubernetes, Docker:**
  Contextual info for cloud/dev workflows.
- **Prompt Symbols:**
  Custom success, error, and Vim mode symbols.

![starship](../images/30.png)

## Usage

### Enable Starship in Your Shell

- **PowerShell:**
  Add this to your `$PROFILE`:
  ```powershell
  Invoke-Expression (&starship init powershell)
  ```
- **Bash:**
  Add this to your `~/.bashrc`:
  ```bash
  eval "$(starship init bash)"
  ```
- **Zsh:**
  Add this to your `~/.zshrc`:
  ```zsh
  eval "$(starship init zsh)"
  ```

### What You Get

- **Beautiful, icon-rich prompt** with Catppuccin colors and Powerline segments
- **Context-aware info**: Git branch/status, language versions, OS, time, Kubernetes, Docker, and more
- **Fast, async rendering** for instant feedback

---

## Frequently Asked Questions (FAQ)

??? question "How do I change the Starship theme?"
    Edit the `palette` and color values in your `starship.toml`. Winfig Dots uses Catppuccin Mocha by default.

??? question "How do I add Starship to my shell?"
    Add the appropriate `starship init` command to your shell profile (see Usage section).

??? question "How do I get the icons to show?"
    Install a Nerd Font and set it as your terminal font.

??? question "How do I customize segments or order?"
    Edit the `format` string in your `starship.toml` to add, remove, or rearrange modules.

??? question "How do I update Starship?"
    Use your package manager (`winget upgrade Starship.Starship`) or download the latest release from GitHub.

??? question "Where is my Starship config file?"
    Usually at `%USERPROFILE%\.config\starship.toml` on Windows or `~/.config/starship.toml` on Linux/macOS.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Starship not found             | Ensure it’s installed and in your PATH. Try restarting your terminal.     |
| Icons not showing              | Install a Nerd Font and set it as your terminal font.                     |
| Colors/theme not applied       | Check your `starship.toml` and terminal color support.                    |
| Prompt not loading             | Ensure you added the `starship init` command to your shell profile.       |
| Git info missing               | Make sure Git is installed and the folder is a Git repo.                  |

If your issue isn’t listed, check the [Starship documentation](https://starship.rs/guide/) or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
