# Ghostty Configuration

My personal Ghostty terminal configuration.

## Current Configuration

```ini
# Ghostty Configuration File

# Font settings
font-family = "JetBrains Mono"
font-size = 14

# Theme - automatically switches based on system light/dark mode
# Solarized Light with custom palette for better diff readability
theme = light:Builtin Solarized Light,dark:rose-pine

# Option 2: Zenbones Light - Soft warm tones with better readability
# theme = light:zenbones_light,dark:rose-pine

# Option 3: Seoulbones Light - Warm paper-like background
# theme = light:seoulbones_light,dark:rose-pine

# Option 4: Gruvbox Light Hard - More contrast, still warm
# theme = light:GruvboxLightHard,dark:rose-pine

# Option 5: Catppuccin Latte - Soft pastels with warm undertones
# theme = light:catppuccin-latte,dark:rose-pine

# Option 6: Rose Pine Dawn (original - softest colors)
# theme = light:rose-pine-dawn,dark:rose-pine

# Increase minimum contrast to ensure text is always readable
minimum-contrast = 3.0

# Window settings
window-padding-x = 10
window-padding-y = 10

# Cursor
cursor-style = block
cursor-style-blink = true

# Shell
command = /bin/bash

# Other settings
copy-on-select = true
confirm-close-surface = true

# Keybindings - Using Ctrl for Linux compatibility
keybind = ctrl+shift+c=copy_to_clipboard
keybind = ctrl+shift+v=paste_from_clipboard
keybind = ctrl+shift+n=new_window
keybind = ctrl+shift+t=new_tab
keybind = ctrl+shift+w=close_surface
keybind = ctrl+shift+q=quit
keybind = ctrl+shift+f=toggle_fullscreen
keybind = shift+enter=text:\n
```

## Last Updated
2025-06-18 18:23:43 UTC
