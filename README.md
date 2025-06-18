# Ghostty Configuration

My personal Ghostty terminal configuration with automatic light/dark theme switching.

## Features

- **Automatic theme switching** based on system light/dark mode
- **Rose Pine themes** (Dawn for light, standard for dark)
- **JetBrains Mono font** at 14pt
- **Comfortable padding** for better readability
- **Linux-friendly keybindings** using Ctrl instead of Super/Cmd

## Installation on Arch Linux

### 1. Install Ghostty

```bash
# Install from AUR (using yay)
yay -S ghostty-git

# Or using paru
paru -S ghostty-git

# Or manually from AUR
git clone https://aur.archlinux.org/ghostty-git.git
cd ghostty-git
makepkg -si
```

### 2. Clone this configuration

```bash
# Clone the repository
git clone git@github.com:marcusziade/ghostty-config.git

# Create the config directory if it doesn't exist
mkdir -p ~/.config/ghostty

# Copy the config file
cp ghostty-config/config ~/.config/ghostty/config
```

### 3. Install JetBrains Mono font (if not already installed)

```bash
# Install via pacman
sudo pacman -S ttf-jetbrains-mono

# Or install the Nerd Font version for additional icons
yay -S ttf-jetbrains-mono-nerd
```

### 4. Launch Ghostty

```bash
ghostty
```

## Alternative Theme Options

The config includes several commented-out theme options you can try:

1. **Catppuccin** - Modern and popular
   ```
   theme = light:catppuccin-latte,dark:catppuccin-mocha
   ```

2. **Tokyo Night** - Vibrant colors
   ```
   theme = light:tokyonight-day,dark:tokyonight
   ```

3. **Nord** - Cool, arctic-inspired
   ```
   theme = light:nord-light,dark:nord
   ```

4. **Dracula/GitHub Light** - High contrast
   ```
   theme = light:GitHub Light,dark:Dracula
   ```

To use a different theme, just uncomment the line you want and comment out the current theme.

## Customization

- **Font size**: Change `font-size = 14` to your preferred size
- **Padding**: Adjust `window-padding-x` and `window-padding-y`
- **Shell**: The config uses bash by default. Change `command = /bin/bash` to your preferred shell (e.g., `/bin/zsh`, `/usr/bin/fish`)

## Keybindings

All keybindings use `Ctrl+Shift` for Linux compatibility:

- `Ctrl+Shift+C` - Copy
- `Ctrl+Shift+V` - Paste
- `Ctrl+Shift+N` - New window
- `Ctrl+Shift+T` - New tab
- `Ctrl+Shift+W` - Close current tab/window
- `Ctrl+Shift+Q` - Quit Ghostty
- `Ctrl+Shift+F` - Toggle fullscreen

## Troubleshooting

If Ghostty doesn't pick up the configuration:

1. Ensure the config is in the correct location: `~/.config/ghostty/config`
2. Check for syntax errors: `ghostty +validate-config`
3. View the current configuration: `ghostty +show-config`

## Notes

- On macOS, Ghostty may use `~/Library/Application Support/com.mitchellh.ghostty/config` instead
- The theme switching requires your desktop environment to properly report light/dark mode to applications
