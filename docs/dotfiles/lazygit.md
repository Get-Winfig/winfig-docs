<h1 align="center">Lazygit: The Ultimate Terminal Git UI</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**Lazygit** is a fast, intuitive, and feature-rich terminal UI for Git. It lets you stage, commit, rebase, resolve conflicts, and manage branches—all with a beautiful, keyboard-driven interface. With Winfig Dots, Lazygit is pre-configured for a modern look, Catppuccin theme, and advanced workflow.

---

## Features

- **Catppuccin Themed UI:** Custom colors and highlights for a beautiful, modern experience.
- **Keyboard-Driven Workflow:** Navigate, stage, commit, and manage branches with powerful keybindings.
- **Rich Side Panels:** View diffs, logs, stashes, and more in split or flexible layouts.
- **Custom Commands:** Open files in VS Code, view GitHub repos, and more with a single key.
- **Emoji & Unicode Support:** Full support for icons and emoji in commit messages and UI.
- **Auto GPG/SSH Integration:** Works seamlessly with your Winfig Git and GPG setup.
- **Configurable Panels & Layouts:** Flexible side/main panel splits, line wrapping, and more.
- **Fast & Lightweight:** Minimal resource usage, instant startup.

---

## Requirements

- [x] [Lazygit](https://github.com/jesseduffield/lazygit) installed on Windows 11
- [x] [GitHub CLI](https://cli.github.com/) for GitHub integration and custom commands
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) installed for dotfile management
- [x] Administrator privileges for certain configurations
- [x] Internet access for downloading dependencies

!!! tip "Quick Install"
    - **Lazygit:**
      `winget install --id JesseDuffield.Lazygit -e`
    - **Git:**
      `winget install --id Git.Git -e`
    - **GitHub CLI:**
      `winget install --id GitHub.cli -e`
    - **PowerShell 7 (optional, recommended):**
      `winget install --id Microsoft.Powershell -e`

---

## Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Lazygit/setup.ps1 | Invoke-Expression
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
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-dots/refs/heads/main/Lazygit/setup.ps1" -OutFile "setup.ps1"
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

- **Catppuccin Theme:**
  Lazygit is themed with Catppuccin colors for borders, highlights, and diffs.
- **Custom Keybindings:**
  Extensive keyboard shortcuts for every action—navigate, stage, commit, rebase, open in VS Code, and more.
- **Panel & Layout Tweaks:**
  Flexible side/main panel splits, line wrapping, and dashboard view.
- **Custom Commands:**
  Open GitHub repo in browser (`B`), open file in VS Code (`V`), and more.
- **Emoji Parsing:**
  Commit messages and UI support emoji and icons.
- **Auto GPG/SSH Integration:**
  Works seamlessly with your Winfig Git and GPG setup.

---

![Lazygit](../images/29.png)

## Usage

### Launch Lazygit

- Open a terminal in your project folder and run:
  ```sh
  lazygit
  ```


### Key Features in Use

- **Navigate panels:** Use <kbd>Arrow Keys</kbd>, <kbd>Tab</kbd>, and <kbd>Shift</kbd>+<kbd>Tab</kbd> to move between panels.
- **Stage/unstage files:** Press <kbd>Space</kbd> or <kbd>S</kbd>.
- **Commit:** Press <kbd>C</kbd> to commit, <kbd>A</kbd> to amend, <kbd>Shift</kbd>+<kbd>C</kbd> to open commit editor.
- **Push/pull:** Press <kbd>P</kbd> to push, <kbd>p</kbd> to pull.
- **Branch management:** Switch, create, or merge branches with intuitive shortcuts.
- **Open in VS Code:** Select a file and press <kbd>V</kbd>.
- **Open GitHub repo:** Press <kbd>B</kbd> from anywhere.
- **Emoji in commits:** Type emoji in commit messages for extra flair.

---

## Advanced Tips

- **Customize further:** Edit your `lazygit.yml` to tweak colors, keybindings, and panel layouts.
- **Use with Winfig Git:** Lazygit works seamlessly with your signed commits, Catppuccin diffs, and GPG/SSH setup.
- **Command log:** Toggle the command log for transparency on every Git action.
- **Split diff view:** Use split or unified diff modes for better code review.
- **Update regularly:** Stay up to date for new features and bug fixes.

---

## Frequently Asked Questions (FAQ)

??? question "How do I change the Lazygit theme?"
    Edit the `theme` section in your `lazygit.yml` to use your favorite Catppuccin palette or custom colors.

??? question "How do I open files in VS Code from Lazygit?"
    Select a file and press <kbd>V</kbd> (custom command in your config).

??? question "How do I open the GitHub repo in my browser?"
    Press <kbd>B</kbd> from anywhere in Lazygit (custom command in your config).

??? question "Can I use emoji in commit messages?"
    Yes! Lazygit supports emoji and icons in commit messages and UI.

??? question "How do I update Lazygit?"
    Use your package manager (`winget upgrade JesseDuffield.Lazygit`) or download the latest release from GitHub.

??? question "Where is my Lazygit config file?"
    Usually at `~/.config/lazygit/config.yml` or `lazygit.yml` in your home directory.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Lazygit not found              | Ensure it’s installed and in your PATH. Try restarting your terminal.     |
| Theme/colors not applied       | Check your `lazygit.yml` config and terminal color support.               |
| Keybindings not working        | Review your config for conflicts or typos.                                |
| Cannot open files in VS Code   | Ensure VS Code is installed and in your PATH.                             |
| Git/GPG integration fails      | Make sure your Git and GPG are set up via Winfig and available in PATH.   |
| Emoji/icons not showing        | Use a Nerd Font and a Unicode-capable terminal.                           |

If your issue isn’t listed, check the [Lazygit documentation](https://github.com/jesseduffield/lazygit#readme) or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
