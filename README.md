# Nagai Poolside — Neovim colorscheme

Nagai Poolside pairs twilight teal surfaces with bright pool-blue accents and sunset corals. Ships as a standalone Neovim colorscheme with optional statusline integrations.

[![Neovim](https://img.shields.io/badge/Neovim-%3E%3D0.9-57A143?logo=neovim)](https://neovim.io)

## Usage

### Lazy.nvim
```lua
return {
  {
    "omarchy/nagai-poolside-nvim",
    priority = 1000,
    config = function()
      require("nagai_poolside").setup({ transparent = false })
      vim.cmd.colorscheme("nagai-poolside")
    end,
  },
}
```

### packer.nvim
```lua
use({
  "omarchy/nagai-poolside-nvim",
  config = function()
    require("nagai_poolside").setup({ transparent = false })
    vim.cmd.colorscheme("nagai-poolside")
  end,
})
```

### vim-plug
```vim
Plug 'omarchy/nagai-poolside-nvim'
lua <<'LUA'
require("nagai_poolside").setup({ transparent = false })
vim.cmd.colorscheme("nagai-poolside")
LUA
```

## Options
- `transparent` (boolean): if `true`, editor backgrounds are left untouched.
- `user_overrides` (function): optional callback run after the theme applies highlights.

## Extras
- Lualine theme: `require('lualine').setup({ options = { theme = 'nagai-poolside' } })`
- Mini.statusline mode colors and built-in highlight groups for common LazyVim plugins.

## Palette
See [`lua/nagai_poolside/palette.lua`](lua/nagai_poolside/palette.lua) for canonical color definitions.

## License
Released under the MIT license. See [LICENSE](LICENSE).
