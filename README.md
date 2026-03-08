# nvim

My personal neovim configuration, based on [nvim-lite](https://github.com/radleylewis/nvim-lite/blob/master/init.lua).

## Design Philosophy

### Single-file configuration
Everything lives in one `init.lua`. No split lua modules, no `lua/` subdirectory hierarchy. The trade-off is simplicity and portability over modularity, the entire config can be read top-to-bottom as one coherent document.

### Native tooling over plugins
The config uses Neovim's built-in `vim.pack` (0.11+) for package management, native LSP (`vim.lsp.config`, `vim.lsp.enable`) over wrapper plugins like lsp-zero, and a hand-crafted statusline rather than lualine or feline. The philosophy is to lean on what Neovim provides before reaching for a plugin.

### Curated, purposeful plugin set
Plugins are chosen to fill specific gaps rather than for convenience:
- `mini.nvim` — a modular utility library covering comments, surround, pairs, indent, buffers, icons, and notifications
- `nvim-treesitter` — syntax highlighting and expression-based folding
- `fzf-lua` — fuzzy finding for files, grep, buffers, LSP symbols, and diagnostics
- `nvim-tree.lua` — file explorer
- `gitsigns.nvim` — git hunk signs, staging, blame, and diff
- `blink.cmp` — Rust-based completion engine with LuaSnip snippet support
- `efm-langserver` + `efmls-configs-nvim` — unified linting and formatting via a single LSP server
- `mason.nvim` — LSP/tool installer
- `kanagawa.nvim` — colorscheme
- `windsurf.vim` — AI code assistance
- `which-key.nvim` — keybinding discoverability
