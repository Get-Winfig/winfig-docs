<h1 align="center">Winfig Neovim: Terminal Based Editor</h1>

![Winfig Banner](images/Banner.png)

<div align="center">

  <strong>Complete Windows 11 configuration ecosystem for clean installations and enterprise-ready development environments</strong>
</div>

---

## Overview
The **Winfig Neovim** module provides a comprehensive setup for Neovim on Windows 11, tailored for both personal and enterprise development environments. This module ensures that Neovim is configured with essential plugins, settings, and themes to enhance productivity and streamline the coding experience.

---

## Features
- [x] **Lazy vim**: A modern Neovim configuration framework that simplifies plugin management and configuration.
- [x] **Pre-configured Plugins**: Includes popular plugins for code completion, syntax highlighting, file navigation, and more.
- [x] **Custom Keybindings**: Optimized keybindings for efficient navigation and editing.
- [x] **Theming**: Aesthetic themes and color schemes for a visually appealing coding environment.
- [x] **Cross-Platform Compatibility**: Configurations that work seamlessly across different operating systems.
- [x] **Enterprise Ready**: Settings and plugins that cater to enterprise development needs, including version control and collaboration tools.

---

##  Requirements

- [x] [Windows Terminal](https://aka.ms/terminal) Modern terminal for Windows
- [x] [Git](https://git-scm.com/download/win) Version control system
- [x] Administrator privileges  Required for certain configurations
- [x] Internet access  For downloading dependencies
- [x] [Nerd Fonts (FiraCode)](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/FiraCode.zip)  Enhanced terminal appearance (see [Nerd Fonts site](https://www.nerdfonts.com/font-downloads) for more options)
- [x] [tree-sitter-cli](https://github.com/nvim-treesitter/nvim-treesitter/tree/main?tab=readme-ov-file#requirements) & a [C compiler](https://visualstudio.microsoft.com/visual-cpp-build-tools/)  For advanced syntax highlighting (optional but recommended)
- [x] [curl](https://curl.se/windows/)  For [blink.cmp](https://github.com/hrsh7th/nvim-cmp) completion engine
- [x] [lazygit](https://github.com/jesseduffield/lazygit/releases)   Terminal Git UI
- [x] For [fzf-lua](https://github.com/ibhagwan/fzf-lua):
    - [ ] [fzf](https://github.com/junegunn/fzf) (v0.25.1 or greater)
    - [ ] [ripgrep](https://github.com/BurntSushi/ripgrep) for live grep
    - [ ] [fd](https://github.com/sharkdp/fd) for fast file finding

!!! tip "Quick Install"
    - **Windows Terminal:**
      `winget install --id Microsoft.WindowsTerminal -e`
    - **Git:**
      `winget install --id Git.Git -e`
    - **Nerd Fonts:**
      Download from [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.4.0/FiraCode.zip) and install your favorite patched font
---

## Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-nvim/main/setup.ps1 | Invoke-Expression
    ```

    !!! success "Why Web Install?"
        - Always gets the latest version
        - No manual download required
        - Automatic script verification
    ![Web Install Demo](images/19.png)

=== "Local Install"

    **Download and run manually** for offline environments:

    ```powershell title="1. Set Execution Policy"
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```

    ```powershell title="2. Download Script"
    # Download from GitHub
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-nvim/main/setup.ps1" -OutFile "setup.ps1"
    ```

    ```powershell title="3. Unblock and Run"
    Unblock-File -Path .\setup.ps1
    .\setup.ps1
    ```

    !!! warning "Note"
        - Ensure you have the latest script version
        - Manual updates required for new releases
        - Verify script integrity before running
    ![Local Install Demo](images/20.png)

=== "Manual Install"

    **Step-by-step manual setup** for full control:

    1. **Install Prerequisites**: Ensure all requirements are met (see [Requirements](#requirements)).
    2. **Clone Configuration**: Clone the Winfig Neovim configuration repository:

        === "Windows"

            ```powershell
            git clone https://github.com/Get-Winfig/winfig-nvim.git $env:LOCALAPPDATA\nvim
            ```

        === "Linux / macOS"

            ```bash
            git clone https://github.com/Get-Winfig/winfig-nvim.git ~/.config/nvim
            ```
---

## Post-Installation

1. **Launch Neovim**: Open Neovim to trigger plugin installation and configuration setup.
2. **Install Plugins**: Follow on-screen prompts to install necessary plugins.
3. **Customize Keybinds**: Modify `lua/config/keybinds.lua` and other configuration files as needed.
4. **Configure Settings**: Adjust Neovim settings in `lua/config/options.lua` to your liking.
5. **Set Up Language Servers**: Install and configure language servers for your preferred programming languages.
6. **Explore Features**: Familiarize yourself with the pre-configured plugins and features.
7. **Enjoy Coding**: Start coding with your newly configured Neovim environment!

![Winfig Neovim](images/22.png)
---

## Keybindings

Winfig Neovim uses [LazyVim](https://www.lazyvim.org) as its base configuration, which comes with a set of [default keybindings](https://www.lazyvim.org/keymaps). Below are the custom keybindings added by Winfig Neovim:

### General Editing
| Keybinding         | Description                             | Mode             |
|--------------------|-----------------------------------------|------------------|
|  <kbd>Space</kbd>  | Leader Key                              | Normal, Visual   |
|  <kbd>;</kbd>      | Enter command mode                      | Normal           |
|  <kbd>Esc</kbd>    | Clear search highlights                 | Normal           |
|  <kbd>Ctrl+f</kbd> | Search and replace with confirmation    | Normal           |
|  <kbd>Ctrl+r</kbd> | Search and replace all occurrences      | Normal           |
|  <kbd>Ctrl+F</kbd> | Find word under cursor                  | Normal           |
|  <kbd>Ctrl+Alt+f</kbd> | Find word under cursor in all files | Normal           |
|  <kbd>Ctrl+z</kbd> | Undo last action                        | Normal           |
|  <kbd>Ctrl+y</kbd> | Redo last undone action                 | Normal           |
|  <kbd>Ctrl+a</kbd> | Select all text in the file             | Normal           |
|  <kbd>Ctrl+c</kbd> | Copy selection to clipboard             | Normal, Visual   |
|  <kbd>Ctrl+x</kbd> | Cut selection to clipboard              | Normal, Visual   |
|  <kbd>Ctrl+v</kbd> | Paste from clipboard                    | Normal, Visual   |
|  <kbd>Alt+j</kbd>  | Move line/selected text down            | Normal, Visual   |
|  <kbd>Alt+k</kbd>  | Move line/selected text up              | Normal, Visual   |

### Buffer, Window, and Tab Management
| Keybinding         | Description                             | Mode             |
|--------------------|-----------------------------------------|------------------|
|  <kbd>Ctrl+w</kbd>+<kbd>l</kbd> | Toggle line wrapping        | Normal           |
|  <kbd>Alt+Tab</kbd>| Switch to the next tab                  | Normal           |
|  <kbd>Alt+1</kbd>  | Open a new tab                          | Normal           |
|  <kbd>Alt+q</kbd>  | Close the current tab                   | Normal           |
|  <kbd>Alt+2</kbd>  | Open new vertical split                 | Normal           |
|  <kbd>Alt+3</kbd>  | Open new horizontal split               | Normal           |
|  <kbd>Shift+q</kbd>| Close the active pane                   | Normal           |
|  <kbd>Ctrl+o</kbd> | Open file in current directory          | Normal           |
|  <kbd>Ctrl+s</kbd> | Save file                               | Normal           |
|  <kbd>Ctrl+q</kbd> | Quit Neovim                             | Normal           |
|  <kbd>Ctrl+Shift+q</kbd> | Quit without saving                 | Normal           |
|  <kbd>Ctrl+h</kbd> | Move focus to the left window           | Normal           |
|  <kbd>Ctrl+l</kbd> | Move focus to the right window          | Normal           |
|  <kbd>Ctrl+j</kbd> | Move focus to the lower window          | Normal           |
|  <kbd>Ctrl+k</kbd> | Move focus to the upper window          | Normal           |
|  <kbd>Ctrl+n</kbd> | Next buffer                             | Normal           |
|  <kbd>Ctrl+p</kbd> | Previous buffer                         | Normal           |
|  <kbd>Alt+z</kbd>  | Toggle Line Wrap                        | Normal           |

### Plugin & Feature Shortcuts
| Keybinding         | Description                             | Mode             |
|--------------------|-----------------------------------------|------------------|
|  <kbd>Leader</kbd>+<kbd>T</kbd> | Color Themes Selection      | Normal           |
|  <kbd>Leader</kbd>+<kbd>G</kbd> | Toggle Tagbar                | Normal           |
|  <kbd>Leader</kbd>+<kbd>/</kbd> | Toggle Comment                | Normal           |
|  <kbd>Leader</kbd>+<kbd>mp</kbd> | Toggle Markdown Preview      | Normal           |

### Git & Lazygit
| Keybinding         | Description                             | Mode             |
|--------------------|-----------------------------------------|------------------|
|  <kbd>Leader</kbd>+<kbd>gp</kbd> | Git Push                     | Normal           |
|  <kbd>Leader</kbd>+<kbd>gs</kbd> | Git Status                   | Normal           |
|  <kbd>Leader</kbd>+<kbd>gu</kbd> | Git Pull                     | Normal           |
|  <kbd>Leader</kbd>+<kbd>gd</kbd> | Git Diff File                | Normal           |
|  <kbd>Leader</kbd>+<kbd>gz</kbd> | Git Stash                    | Normal           |
|  <kbd>Leader</kbd>+<kbd>ga</kbd> | Git Add All                  | Normal           |
|  <kbd>Leader</kbd>+<kbd>gc</kbd> | Git Commit                   | Normal           |
|  <kbd>Leader</kbd>+<kbd>gb</kbd> | Git Branch                   | Normal           |
|  <kbd>Leader</kbd>+<kbd>gx</kbd> | Create New Git Branch        | Normal           |
|  <kbd>Leader</kbd>+<kbd>go</kbd> | Checkout Git Branch          | Normal           |
|  <kbd>Leader</kbd>+<kbd>gm</kbd> | Git Merge                    | Normal           |
|  <kbd>Leader</kbd>+<kbd>gi</kbd> | Initialize Git Repo          | Normal           |
|  <kbd>Leader</kbd>+<kbd>gg</kbd> | LazyGit                      | Normal           |
|  <kbd>Leader</kbd>+<kbd>gf</kbd> | LazyGit Current File         | Normal           |
|  <kbd>Leader</kbd>+<kbd>gl</kbd> | LazyGit View Logs            | Normal           |

### Language/Project/Example
| Keybinding         | Description                             | Mode             |
|--------------------|-----------------------------------------|------------------|
|  <kbd>Leader</kbd>+<kbd>co</kbd> | Typescript Organize Imports  | Normal           |
|  <kbd>Leader</kbd>+<kbd>cR</kbd> | Typescript Rename File       | Normal           |

> 💡 *Tip: You can further customize these keybindings in keymaps file!*

---

## Frequently Asked Questions (FAQ)

??? question "How do I update Winfig Neovim?"
    To update Winfig Neovim, you can pull the latest changes from the GitHub repository:

    ```powershell title="Windows"
    cd $env:LOCALAPPDATA\nvim
    git pull origin main
    ```

    ```bash title="Linux / macOS"
    cd ~/.config/nvim
    git pull origin main
    ```

    After pulling the latest changes, restart Neovim to apply the updates.

??? question "How do I add new plugins?"
    You can add new plugins by creating a new Lua file in the `lua/plugins/` directory and specifying the plugin details. After adding the plugin, restart Neovim to install it.

??? question "Can I customize the theme?"
    Yes, you can customize the theme by modifying the theme settings in the `lua/plugins/Themery.lua` file. You can choose from various themes available in the LazyVim framework.

??? question "Where can I find the configuration files?"
    The configuration files are located in the following directory:

    - Windows: `$env:LOCALAPPDATA\nvim`
    - Linux / macOS: `~/.config/nvim`
    - You can edit these files to customize settings, keybindings, and plugins.

??? question "Is there support for language servers?"
    Yes, Winfig Neovim supports Language Server Protocol (LSP) integration.

??? question "How do I report issues or contribute?"
    You can report issues or contribute to the Winfig Neovim project by visiting the [GitHub repository](https://github.com/Get-Winfig/winfig-nvim).

??? question "What if I encounter issues during installation?"
    **If you face any issues,** please check the GitHub repository for troubleshooting tips or open an issue for assistance.

---

## Troubleshooting Guide

If you encounter any issues while using Winfig Terminal, here are some common problems and their solutions:

| Issue                                    | Solution                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------|
| Neovim not launching                     | Ensure Neovim is installed and added to your system PATH.                                   |
| Plugins not installing                   | Check your internet connection and try restarting Neovim.                                  |
| Keybindings not working                  | Verify that the keybindings are correctly defined in the configuration files.               |
| Theme not applying                       | Ensure the theme plugin is installed and configured correctly in the `Themery.lua` file.        |
| Language server not functioning          | Make sure the language server is installed and properly configured in the LSP settings.        |
| Errors during startup                    | Check the Neovim log files for error messages and troubleshoot accordingly.                 |
| Performance issues                       | Disable unnecessary plugins or check for conflicting configurations.                        |
| Git integration not working              | Ensure Git is installed and accessible from the command line.                               |
| Issues with specific plugins             | Refer to the plugin documentation for troubleshooting steps.                                |

