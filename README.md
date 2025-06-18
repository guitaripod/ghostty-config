# Ghostty Configuration

My personal Ghostty terminal configuration.

## Current Configuration

```ini
# Ghostty Configuration File

# Font settings
font-family = "JetBrains Mono"
font-size = 14

# Theme - automatically switches based on system light/dark mode
# Option 1: Rose Pine (soft, pleasant colors)
theme = light:rose-pine-dawn,dark:rose-pine

# Option 2: Catppuccin (modern, popular theme)
# theme = light:catppuccin-latte,dark:catppuccin-mocha

# Option 3: Tokyo Night (vibrant colors)
# theme = light:tokyonight-day,dark:tokyonight

# Option 4: Nord (cool, arctic-inspired)
# theme = light:nord-light,dark:nord

# Option 5: Dracula (high contrast)
# theme = light:GitHub Light,dark:Dracula

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
keybind = ctrl+shift+f=toggle_fullscreen```

## Last Updated
2025-06-18 17:53:30 UTC
