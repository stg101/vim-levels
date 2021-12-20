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
  }
```

keybindings.json

```
  {
    "key": "escape",
    "command": "macros.vimInsertMode",
    "when": "editorTextFocus && !vim.active && !inDebugRepl"
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
- ctr + u : move up half screen
- ctrl + d : move down half screen
- dd : remove and copy
- d + n : remove n lines
- p : paste
- ctrl + enter : empty line below
- [all vs-code commands]
