<h1 align="center">Bat: Modern Catppuccin-Powered File Viewer</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**Bat** is a modern, feature-rich alternative to `cat` for the terminal. It provides beautiful syntax highlighting, Git integration, paging, and theming—making file viewing and code review a delight. With Winfig Dots, Bat is pre-configured with the Catppuccin Mocha theme, advanced filetype mapping, and seamless paging for a premium experience on Windows.

---

## Features

- **Catppuccin Mocha Theme:** Beautiful, modern syntax highlighting for over 100 languages.
- **Advanced Filetype Mapping:** Custom mappings for Markdown, YAML, TOML, INI, JSON, scripts, configs, and more.
- **Paging & Navigation:** Always-on paging with mouse support and smooth navigation via `less`.
- **Git Integration:** Show Git changes in the gutter for quick code review.
- **Line Numbers & Highlighting:** Full support for line numbers, highlighting, and code style.
- **Tabs & Indentation:** Consistent 4-space tabs for all files.
- **Fast & Lightweight:** Instant output, even for large files.

---

## Requirements

- [x] [Bat](https://github.com/sharkdp/bat) installed on Windows 11
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) for Git gutter integration (optional)
- [x] Administrator privileges for certain configurations
- [x] Internet access for downloading dependencies

!!! tip "Quick Install"
    - **Bat:**
      `winget install --id sharkdp.bat -e`
    - **Git:**
      `winget install --id Git.Git -e`
    - **PowerShell 7 (optional, recommended):**
      `winget install --id Microsoft.Powershell -e`

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

## Configuration Highlights

- **Catppuccin Mocha Theme:**
  Bat uses the Catppuccin Mocha theme for a modern, visually appealing look.
- **Full Style & Italics:**
  Always use full style and italic text for code and prose.
- **Tabs:**
  4-space tabs for consistent indentation.
- **Paging:**
  Always-on paging with mouse support via `less`.
- **Filetype Mapping:**
  Extensive custom filetype mapping for accurate syntax highlighting (see below).


## Usage

### Basic Usage

- **View a file with syntax highlighting:**
  ```sh
  bat myfile.py
  ```
- **Show line numbers and Git changes:**
  ```sh
  bat myfile.js
  ```
- **Page through large files with mouse support:**
  ```sh
  bat myfile.md
  ```
- **Use as a drop-in replacement for `cat`:**
  ```sh
  bat README.md
  ```

### Example: Custom Filetype Mapping

Bat is configured to recognize and highlight a wide range of filetypes. For example:

```sh
bat --map-syntax "*.md:Markdown" --map-syntax "*.yml:YAML" --map-syntax "*.ps1:PowerShell" myfile.md
```

All mappings are pre-configured in your Winfig Dots bat config for maximum compatibility.

---

## Configuration Highlights

- **Catppuccin Theme:**
  All diffs, logs, and status outputs are styled with Catppuccin via Delta (`features = catppuccin-macchiato`, `syntax-theme = catppuccin-frappe`).
- **Delta as Pager & Diff Tool:**
  Delta is set as the default pager and diff tool for all relevant commands.
- **VS Code Integration:**
  Both the editor and merge tool are set to VS Code for a seamless experience.
- **GPG Signing:**
  Commits are signed by default for security and authenticity.
- **Global Ignore & Includes:**
  Uses a global `.gitignore` and includes modular config snippets (e.g., Catppuccin settings).
- **Custom Log Format:**
  Logs are decorated with color, author, date, GPG status, and more for clarity.

---

## Frequently Asked Questions (FAQ)

??? question "How do I change the Bat theme?"
    Use the `--theme` flag or set it in your config file. Winfig Dots uses Catppuccin Mocha by default.

??? question "How do I enable paging and mouse support?"
    Paging is always on with the provided config. Mouse support is enabled via the `less` pager.

??? question "How do I add or change filetype mappings?"
    Edit your bat config and add more `--map-syntax` lines as needed.

??? question "How do I use Bat as a cat replacement?"
    Just use `bat` instead of `cat` in your terminal commands.

??? question "How do I update Bat?"
    Use your package manager (`winget upgrade sharkdp.bat`) or download the latest release from GitHub.

??? question "Where is my Bat config file?"
    Usually at `%APPDATA%\bat\config` on Windows or `~/.config/bat/config` on Linux/macOS.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Bat not found                  | Ensure it’s installed and in your PATH. Try restarting your terminal.     |
| Theme/colors not applied       | Check your config and terminal color support.                             |
| Filetype not highlighted       | Add or adjust `--map-syntax` in your config.                              |
| Paging/mouse not working       | Ensure `less` is installed and your terminal supports mouse events.        |
| Git gutter not showing         | Make sure Git is installed and the file is in a Git repo.                 |

If your issue isn’t listed, check the [Bat documentation](https://github.com/sharkdp/bat#readme) or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
