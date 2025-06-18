# Ghostty Installation Guide

## Prerequisites

### Font Installation

This configuration uses JetBrainsMono Nerd Font. Install it first:

#### macOS
```bash
# Using Homebrew
brew tap homebrew/cask-fonts
brew install --cask font-jetbrains-mono-nerd-font
```

#### Arch Linux
```bash
# Install from AUR
yay -S ttf-jetbrains-mono-nerd
# or
paru -S ttf-jetbrains-mono-nerd
```

## Installing Ghostty

### macOS

1. Download the latest release from [Ghostty's website](https://ghostty.org)
2. Open the DMG file and drag Ghostty.app to Applications
3. Launch Ghostty from Applications or Spotlight

### Arch Linux

```bash
# Install from AUR (using yay)
yay -S ghostty-git

# Or using paru
paru -S ghostty-git

# Or build manually from AUR
git clone https://aur.archlinux.org/ghostty-git.git
cd ghostty-git
makepkg -si
```

## Installing This Configuration

### 1. Clone this repository

```bash
git clone https://github.com/marcusziade/ghostty-config.git ~/Dev/ghostty-config
```

### 2. Install the configuration

#### macOS
```bash
# Create config directory
mkdir -p ~/.config/ghostty

# Symlink the config (recommended for easy updates)
ln -sf ~/Dev/ghostty-config/config ~/.config/ghostty/config

# Or copy it
cp ~/Dev/ghostty-config/config ~/.config/ghostty/config
```

#### Arch Linux
```bash
# Create config directory
mkdir -p ~/.config/ghostty

# Symlink the config (recommended for easy updates)
ln -sf ~/Dev/ghostty-config/config ~/.config/ghostty/config

# Or copy it
cp ~/Dev/ghostty-config/config ~/.config/ghostty/config
```

### 3. Verify installation

```bash
# Check if config is loaded correctly
ghostty +validate-config

# View the loaded configuration
ghostty +show-config
```

## Updating Configuration

If you used symlinks:
```bash
cd ~/Dev/ghostty-config
git pull
# Reload Ghostty or restart it
```

If you copied the file:
```bash
cd ~/Dev/ghostty-config
git pull
cp config ~/.config/ghostty/config
# Reload Ghostty or restart it
```

## Features of This Configuration

- **Solarized Light theme** for light mode with enhanced contrast
- **Rose Pine theme** for dark mode
- **JetBrainsMono Nerd Font** for programming ligatures and icons
- **Shift+Enter** creates a new line (useful in REPLs and chat apps)
- **Minimum contrast ratio** of 3.0 for better readability
- **Cross-platform keybindings** using Ctrl+Shift

## Troubleshooting

### Config not loading?
1. Check the config location:
   - macOS/Linux: `~/.config/ghostty/config`
   - macOS (alternative): `~/Library/Application Support/com.mitchellh.ghostty/config`

2. Validate the config:
   ```bash
   ghostty +validate-config
   ```

### Font not working?
1. Verify font installation:
   ```bash
   # List installed fonts
   ghostty +list-fonts | grep -i jetbrains
   ```

2. Try the regular JetBrains Mono if Nerd Font isn't found:
   ```bash
   # Edit config and change:
   font-family = "JetBrains Mono"
   ```

### Theme issues?
- The automatic light/dark switching requires your OS to report the theme correctly
- On Linux, this depends on your desktop environment
- You can manually set a single theme by removing the `light:` and `dark:` prefixes