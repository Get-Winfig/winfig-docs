<h1 align="center">Fastfetch: Blazing-Fast System Info for Windows</h1>

![Winfig Banner](../images/Banner.png)

<div align="center">
  <strong>Part of the Winfig Dots ecosystem for seamless Windows customization and productivity</strong>
</div>

---

## Overview

**Fastfetch** is a blazing-fast, open-source system information tool for Windows, Linux, and macOS. It displays your OS, hardware, desktop environment, and more in a beautiful, customizable ASCII or logo format—perfect for terminal screenshots, dotfiles, and showing off your setup. With Winfig Dots, Fastfetch is pre-configured for Windows 11 and ready to use out of the box.

---

## Features

- **Instant System Info:** See OS, CPU, GPU, RAM, disk, shell, terminal, and more in one command.
- **Custom Logos & ASCII Art:** Display Windows, Linux, or custom logos in your terminal.
- **Highly Configurable:** Tweak colors, modules, output format, and more with config files or command-line flags.
- **Cross-Platform:** Works on Windows, Linux, and macOS.
- **Fast & Lightweight:** Minimal resource usage, instant output.
- **Dotfiles Friendly:** Easily integrate with your dotfiles and scripts for a personalized look.

---

## Requirements

- [x] [Fastfetch](https://github.com/fastfetch-cli/fastfetch/) installed on Windows 11
- [x] [PowerShell 5+](https://github.com/PowerShell/PowerShell) for automation and scripting
- [x] [Git](https://git-scm.com/download/win) installed for dotfile management
- [x] Administrator privileges for certain configurations
- [x] Internet access for downloading dependencies

!!! tip "Quick Install"
    - **Fastfetch:**
      `winget install --id Fastfetch-cli.Fastfetch -e`
    - **Git:**
      `winget install --id Git.Git -e`
    - **PowerShell 7 (optional, recommended):**
      `winget install --id Microsoft.Powershell -e`


---

## Installation Methods

=== "Web Install (Recommended)"

    **One-line installation** - Downloads and runs automatically:

    ```powershell title="Run in Administrative PowerShell"
    Invoke-RestMethod -useb https://raw.githubusercontent.com/Get-Winfig/winfig-dots/main/Fastfetch/setup.ps1 | Invoke-Expression
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
    Invoke-WebRequest -useb "https://raw.githubusercontent.com/Get-Winfig/winfig-dots/main/Fastfetch/setup.ps1" -OutFile "setup.ps1"
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

## Usage

After installation, open a terminal and run:

```powershell
fastfetch
```

You’ll see a beautiful summary of your system info with a Custom logo.

![Fastfetch](../images/27.png)

To use a custom config, edit your Fastfetch config file or pass options via command line. Integrate Fastfetch in your PowerShell profile or dotfiles for instant system info on startup.

---

## Frequently Asked Questions (FAQ)

??? question "How do I customize the Fastfetch output?"
    Use command-line flags (see `fastfetch --help`) or edit your config file for colors, modules, and logo.

??? question "Can I use Fastfetch on Linux or macOS?"
    Yes! Fastfetch is cross-platform and works on Windows, Linux, and macOS.

??? question "Where is the Fastfetch config file?"
    By default, it’s in your user profile folder. You can specify a custom config with `--config`.

??? question "How do I update Fastfetch?"
    Re-run the install script or use `winget upgrade Fastfetch-cli.Fastfetch`.

??? question "How do I show a custom logo?"
    Use the `--logo` flag, e.g. `fastfetch --logo Windows` or `fastfetch --logo <your-logo>`.

---

## Troubleshooting

| Issue                          | Solution                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Fastfetch not found             | Ensure it’s installed and in your PATH. Try restarting your terminal.     |
| Output looks wrong              | Check your terminal font and encoding. Use a Nerd Font for best results.  |
| Modules missing                 | Update Fastfetch or check your config for correct module names.           |
| Script fails to run             | Run PowerShell as Administrator and check your execution policy.          |
| Logo not showing                | Use the `--logo` flag and verify your terminal supports Unicode/ASCII art.|

If your issue isn’t listed, check the [Fastfetch documentation](https://github.com/fastfetch-cli/fastfetch#readme) or [Winfig GitHub Issues](https://github.com/Get-Winfig/winfig-docs/issues).
