NeoClear.lua
-----

Save you from both:
- the tree-sitter bug on folding, see: https://github.com/nvim-treesitter/nvim-treesitter/issues/2439
- the "how to clear the last highlight qq" problem

## DEMO

https://user-images.githubusercontent.com/24765272/152267526-7ebe6876-cf89-40ed-ae64-f639153eeefe.mov

## Features

- Only one command, since this is a temporary patch.
- Can be run on "un-saved" buffer without error(as `silent!`)
  - but you still need to save the buffer to solve the folding bug.
- Leave window-view intact after run.

## Usage


```lua
NeoClear
```

example

```lua
vim.keymap.set('n', '<C-C>', function()
  vim.cmd('NeoClear')
end, { noremap = true, silent = true, nowait = true })
```
