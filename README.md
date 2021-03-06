# vim-levels

## Setup

Setup to make vscode commands work alongside vim

Install macros extension


setting.json

```
  "vim.useCtrlKeys": true,
  "vim.handleKeys": {
    "<C-u>": true
  },
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["i"],
      "after": ["i"],
      "commands": ["toggleVim"]
    }
  ],
  "editor.lineNumbers": "relative",
  "macros": {
    "vimInsertMode": ["toggleVim", "extension.vim_escape"]
  }
```

keybindings.json

```
  {
    "key": "escape",
    "command": "macros.vimInsertMode",
    "when": "editorTextFocus && !vim.active && !inDebugRepl"
  },
    {
    "key": "ctrl+k",
    "command": "workbench.action.focusActiveEditorGroup",
    "when": "terminalFocus"
  },
  {
    "key": "ctrl+k",
    "command": "workbench.action.terminal.focus",
    "when": "!terminalFocus"
  },
  {
    "key": "alt+f2",
    "command": "workbench.action.quickSwitchWindow"
  }
```

## Level 1

Value: fast movements in file
Flow: [Esc] --> move --> i

- hjkl : basic_moves
- n + basic_move : repeat n times move
- w : move word by word (start)
- b : move word by word backwards (start)
- e : move word by word (end)
- ge : move word by word backwards (end)
- gg : go to start of file
- G : go to end of file
- ctr + u : move up half screen
- ctrl + d : move down half screen
- dd : remove and copy
- d + n : remove n lines
- p : paste
- [all vs-code commands]
- ctrl + enter : empty line below
- alt + direction_arrow : switch terminals

### Windows

![windows commands](windows-commands.png)

## Level 2

### tmux

prefix: ctrl + b

![tmux commands](tmux-commands.png)