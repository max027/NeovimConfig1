# Neovim Configuration

A simple and efficient Neovim configuration focused on productivity and ease of use.

## Requirements

- Neovim >= 0.9.0
- Git
- A [Nerd Font](https://www.nerdfonts.com/) (optional, for icons)
- ripgrep (for Telescope text search)

## Installation

### Backup existing configuration

```bash
mv ~/.config/nvim ~/.config/nvim.backup
mv ~/.local/share/nvim ~/.local/share/nvim.backup
```

### Clone this repository

```bash
git clone https://github.com/max027/NeovimConfig1.git ~/.config/nvim
```

### Start Neovim

```bash
nvim
```

Plugins will automatically install on first launch.

## Key Mappings

### General
- `<Space>` - Leader key

### File Navigation
- `<leader>e` - Toggle file explorer
- `<leader>ff` - Find files
- `<leader>fg` - Live grep
- `<leader>fb` - Find buffers

### LSP
- `gd` - Go to definition
- `gr` - Go to references
- `K` - Hover documentation
- `<leader>ca` - Code actions
- `<leader>rn` - Rename symbol


## Customization

Edit the configuration files in `~/.config/nvim/lua/`:

- `init.lua` - Main configuration entry point
- `lua/config/` - Core settings and keymaps
- `lua/plugins/` - Plugin configurations


# Supported Languages
LSP support is configured for:
- Rust
- java



Additional language servers can be added in *lua/plugins/lsp.lua*. For java python must be installed and in path.
## Troubleshooting

### Plugins not loading
```bash
# Remove plugin data and restart
rm -rf ~/.local/share/nvim
nvim
```

### LSP not working
```bash
# Check if language server is installed
:checkhealth lsp
```

### Performance issues
```bash
# Profile startup time
nvim --startuptime startup.log
```

## License

This configuration is released under the MIT License. See [LICENSE](LICENSE) for details.
