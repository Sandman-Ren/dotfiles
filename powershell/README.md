# PowerShell Configuration

This directory contains PowerShell profile configuration with enhanced features including smart directory navigation, beautiful prompts, and Kubernetes shortcuts.

## Prerequisites

Before setting up the PowerShell profile, you'll need to install several dependencies.

### 1. Install Oh-My-Posh

Oh-My-Posh provides beautiful and customizable terminal prompts.

**Using winget (Recommended):**
```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

**Using Chocolatey:**
```powershell
choco install oh-my-posh
```

**Using PowerShell Gallery:**
```powershell
Install-Module oh-my-posh -Scope CurrentUser
```

### 2. Install and Configure a Nerd Font

Nerd Fonts are required for proper icon display in Oh-My-Posh themes.

#### Install Nerd Font

**Option A: Using Oh-My-Posh (Easiest):**
```powershell
oh-my-posh font install
```
Select a font from the list (recommended: `FiraCode Nerd Font` or `CascadiaCode Nerd Font`).

**Option B: Manual Installation:**
1. Download a Nerd Font from [Nerd Fonts website](https://www.nerdfonts.com/font-downloads)
2. Extract the ZIP file
3. Right-click on the font files and select "Install for all users"

#### Configure Windows Terminal

1. Open Windows Terminal
2. Press `Ctrl + ,` to open settings
3. Go to **Profiles** → **Defaults** (or your specific PowerShell profile)
4. Under **Appearance**, set the **Font face** to your installed Nerd Font (e.g., "FiraCode Nerd Font")
5. Save the settings

#### Configure PowerShell Console (Optional)

If using the traditional PowerShell console:
1. Right-click the title bar and select "Properties"
2. Go to the "Font" tab
3. Select your installed Nerd Font
4. Click "OK"

### 3. Install Additional Dependencies

Install the following tools for full functionality:

**Zoxide (Smart directory navigation):**
```powershell
# Using winget
winget install ajeetdsouza.zoxide

# Using Chocolatey
choco install zoxide

# Using Cargo (if you have Rust installed)
cargo install zoxide
```

**Kubernetes Tools:**
```powershell
# kubectl
winget install Kubernetes.kubectl

# kubens (part of kubectx)
choco install kubens

# minikube
winget install Kubernetes.minikube
```

**Chocolatey (if not already installed):**
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

## Installation

### 1. Set Execution Policy

Allow PowerShell to run scripts:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### 2. Install the Profile

**Option A: Direct Copy**
```powershell
# Navigate to the dotfiles directory
cd path\to\dotfiles\powershell

# Copy the profile to your PowerShell directory
Copy-Item .\Microsoft.PowerShell_profile.ps1 $PROFILE -Force
```

**Option B: Symbolic Link (Recommended for development)**
```powershell
# Remove existing profile if it exists
if (Test-Path $PROFILE) { Remove-Item $PROFILE }

# Create symbolic link
New-Item -ItemType SymbolicLink -Path $PROFILE -Target "path\to\dotfiles\powershell\Microsoft.PowerShell_profile.ps1"
```

### 3. Reload PowerShell

Restart your PowerShell session or reload the profile:
```powershell
. $PROFILE
```

## Configuration

### Oh-My-Posh Theme

The profile uses the `iterm2` theme by default. To change the theme:

1. Browse available themes:
   ```powershell
   Get-PoshThemes
   ```

2. Edit the profile and change the theme line:
   ```powershell
   oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\your-theme.omp.json" | Invoke-Expression
   ```

3. Reload the profile:
   ```powershell
   . $PROFILE
   ```

### Custom Theme Location

To use a custom theme file:
```powershell
oh-my-posh init pwsh --config "path\to\your\custom-theme.omp.json" | Invoke-Expression
```

## Features

After installation, you'll have access to:

### Aliases
- `mk` → `minikube`
- `k` → `kubectl`
- `kns` → `kubens`

### Enhanced Navigation
- `z <directory>` - Jump to frequently used directories
- `zi` - Interactive directory picker
- `z -` - Go to previous directory
- `z +` - Go forward in directory history

### Beautiful Prompt
- Git status integration
- Current directory display
- Execution time for long-running commands
- Error status indicators

## Troubleshooting

### Fonts Not Displaying Correctly
- Ensure you've installed a Nerd Font
- Verify the font is selected in your terminal settings
- Restart your terminal application

### Oh-My-Posh Not Loading
- Check if Oh-My-Posh is installed: `oh-my-posh version`
- Verify the theme path exists: `Test-Path "$env:POSH_THEMES_PATH\iterm2.omp.json"`
- Check PowerShell execution policy: `Get-ExecutionPolicy`

### Zoxide Not Working
- Ensure zoxide is installed: `zoxide --version`
- Add zoxide to your PATH if needed
- Restart PowerShell after installation

### Permission Errors
- Run PowerShell as Administrator for installation
- Check execution policy settings
- Ensure you have write permissions to the profile directory

## Customization

Feel free to modify the `Microsoft.PowerShell_profile.ps1` file to add your own:
- Custom aliases
- Additional functions
- Module imports
- Environment variables

The profile is designed to be easily extensible for your specific needs.
