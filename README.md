# null.nvim

An empty plugin specification for Neovim that won't execute anything.

This plugin is similar to zdharma contentuum/null.

**Example uses:**

When you want to add additional options to certain plugins based on conditions
(in lazy.nvim, you can use 'enabled' to enable when conditions are met)

```lua
return {
  "MaJinjie/null.nvim",
  enabled = vim.g.neovide or false,
  specs = {
    "AstroNvim/astrocore",
    ---@param opts AstroCoreOpts
    opts = function(_, opts) end,
  },
}
```

Only when using Neovide to open Neovim will the options related to Neovide take effect.
