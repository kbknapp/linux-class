# Vim Cheat Sheet

## CRITICAL

| Key | Function |
| :---: | :--- |
| `esc` | Command Mode |
| `i`   | Insert Mode |
| `v`   | Visual (Select) Mode |
| `:`   | Enter Command |

## Global (COMMAND MODE)

| Key   | Function |
| :---: | :---     |
| `:q`  | Quit     |
| `:q!` | Force Quit (Discard Changes) |
| `:wq` | Save and Quit |
| `:w`  | Save |

## Cursor movement (COMMAND MODE)

| Key   | Function |
| :---: | :---     |
| `h`   | move cursor left |
| `j`   | move cursor down |
| `k`   | move cursor up |
| `l`   | move cursor right |
| `w`   | jump forwards to the start of a word |
| `e`   | jump forwards to the end of a word |
| `b`   | jump backwards to the start of a word |
| `0`   | jump to the start of the line |
| `^`   | jump to the first non-blank character of the line |
| `$`   | jump to the end of the line |
| `gg`  | go to the first line of the document |
| `G`   | go to the last line of the document |
| `5G`  | go to line 5 |
| `fx`  | jump to next occurrence of character x |
| `Fx`  | jump to previous occurence of character x |

* *Tip: Prefix a cursor movement command with a number to repeat it. For example, `4j` moves down 4 lines.*


## Entering Insert mode (inserting/appending text)

| Key   | Function |
| :---: | :---     |
| `i`   | insert before the cursor |
| `I`   | insert at the beginning of the line |
| `a`   | insert (append) after the cursor |
| `A`   | insert (append) at the end of the line |
| `o`   | append (open) a new line below the current line |
| `O`   | append (open) a new line above the current line |
| `esc` | exit insert mode |

## Editing

| Key   | Function |
| :---: | :---     |
| `r`   | replace a single character|
| `J`   | join line below to the current one with one space in between|
| `ci[` | Change "inside" `[` and `]` (other brackets work too, or quotes)|
| `cc`  | change (replace) entire line|
| `cw`  | change (replace) to the end of the word|
| `c$`  | change (replace) to the end of the line|
| `s`   | delete character and substitute text|
| `u`   | undo|
| `Ctrl + r` | redo|
| `.`   | repeat last command|

* Think in "sentences"
* "Change Inside Parens" = `ci(`

## Selecting Text (VISUAL mode)

| Key   | Function |
| :---: | :---     |
| `v` | start visual mode|
| `V` | start line visual mode |
| `>` | shift text right |
| `<` | shift text left |
| `y` | yank (copy) marked text |
| `d` | delete marked text |
| `~` | switch case |
| `esc` | exit visual mode |

* *Tip: Once in VISUAL MODE normal movement commands work to move selection cursor*

## Cut and paste

| Key   | Function |
| :---: | :---     |
| `yy`  | yank (copy) a line |
| `2yy` | yank (copy) 2 lines |
| `yw`  | yank (copy) the characters of the word from the cursor position to the start of the next word |
| `y$`  | yank (copy) to end of line |
| `p`   | put (paste) the clipboard after cursor |
| `P`   | put (paste) before cursor |
| `dd`  | delete (cut) a line |
| `2dd` | delete (cut) 2 lines |
| `dw`  | delete (cut) the characters of the word from the cursor position to the start of the next word |
| `D`   | delete (cut) to the end of the line |
| `d$`  | delete (cut) to the end of the line |
| `ci[` | Change "inside" `[` and `]` (other brackets work too, or quotes)|
| `x`   | delete (cut) a single character |

* Think in "sentences"
  * "Delete Inside Parens" = `di(`
  * "Select (visual) inside quotes, yank (copy), move down 5 lines, and put (paste)" = `vi"5jp`

## Search and replace

| Key   | Function |
| :---: | :---     |
| `/pattern` | search for `pattern` |
| `?pattern` | search backward for `pattern` |
| `n` | repeat search in same direction |
| `N` | repeat search in opposite direction |
| `:%s/old/new/g` | replace all old with new throughout file |
| `:%s/old/new/gc` | replace all old with new throughout file with confirmations |
| `:nohl` | remove highlighting of search matches |

## Macros

| Key   | Function |
| :---: | :---     |
| `qa`  | record macro `a` |
| After `qa` then `q`   | stop recording macro `a` |
| `@a`  | run macro `a` |
| `@@`  | rerun last run macro |

