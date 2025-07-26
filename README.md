# Dotfiles

Personal configuration files for Windows PowerShell environment.

## What's Included

### PowerShell Profile (`powershell/Microsoft.PowerShell_profile.ps1`)

- **Kubernetes Aliases**: Quick shortcuts for container orchestration
  - `mk` → `minikube`
  - `k` → `kubectl`
  - `kns` → `kubens`

- **Directory Navigation**: Enhanced with [zoxide](https://github.com/ajeetdsouza/zoxide)
  - `z <directory>` - Smart directory jumping
  - `zi` - Interactive directory search

- **Terminal Enhancement**: [Oh My Posh](https://ohmyposh.dev/) integration
  - Uses the `iterm2` theme for a beautiful prompt

- **Package Management**: Chocolatey profile integration

## Quick Start

1. Clone this repository:
   ```bash
   git clone https://github.com/Sandman-Ren/dotfiles.git
   ```

2. **For PowerShell setup**: See detailed instructions in [`powershell/README.md`](./powershell/README.md)
   - Includes Oh-My-Posh installation and configuration
   - Nerd Font setup for Windows Terminal
   - Complete dependency installation guide

## Dependencies

The PowerShell configuration requires several tools. See [`powershell/README.md`](./powershell/README.md) for detailed installation instructions.

**Core Dependencies:**
- [Oh My Posh](https://ohmyposh.dev/) - Terminal prompt customization
- [zoxide](https://github.com/ajeetdsouza/zoxide) - Smart directory navigation
- [Nerd Font](https://www.nerdfonts.com/) - For proper icon display
- [Chocolatey](https://chocolatey.org/) - Package manager for Windows

**Optional Tools:**
- [kubectl](https://kubernetes.io/docs/tasks/tools/) - Kubernetes command-line tool
- [kubens](https://github.com/ahmetb/kubectx) - Kubernetes namespace switcher
- [minikube](https://minikube.sigs.k8s.io/) - Local Kubernetes cluster

## Usage

After installation, restart your PowerShell session to load the new configuration. You'll have access to all the aliases and enhanced navigation features.
