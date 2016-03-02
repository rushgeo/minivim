# MiniVim

Customized by rushgeo, see command table

*Click to launch an Youtube video demo:*

[![A screenshot](https://raw.githubusercontent.com/sd65/MiniVim/master/Screenshot.png)](https://www.youtube.com/watch?v=n0h_3e0FfYk)

## Goals

- No bullshit default key mappings
- Mimic Sublime Text / Shell key mappings
- Minimal: one file, **no plugin needed!**

## Automated setup

- Clone this repo to the folder of your choice:

`git clone git@github.com:sd65/MiniVim.git`

- Go inside this repo:

`cd MiniVim`

- Launch the install script and follow the instructions:

`./install.sh`

- It's ready! :smile: Launch Vim:

`vim`

## Manual setup

If you can't clone the repo and do the above steps, just download the .vimrc to your home dir (backup your current .vimrc before).

`wget https://raw.githubusercontent.com/sd65/MiniVim/master/vimrc -O ~/.vimrc`

And then add `stty -ixon` to your .zshrc or .bashrc (your shell will ignore XON/XOFF signals. Needed to remap Ctrl S, Ctrl Q).

## How to use

- **The key mappings can be used in Insert, Normal and Visual mode (yes, no need to exit Insert or Visual mode)**
- Vim launched by in Insert mode ONLY WHEN OPENING A NEW TAB
- The mouse can be used in Normal and Visual mode to scroll, select, change tab and more.
- There are clear visual hints on which mode you currently using. Like pink=normal, blue=insert and green=visual...

### General Mappings

Keys | Action | Comments         
| :---: | :---: | :---: |
| **Moving** | **----------** | **----------**
`Arrows` | Move the cursor | Like every editor
`Ctrl Arrows` | Move the cursor *fast*. | Ctrl L/R skips words, Ctrl U/D skips 20 lines
`PageUp/Down` | Skip 50 lines up/down. | Default behavior? Commented out right now.
`Ctrl A` | Go to the beginning of the line | As in Nano/Shell
`Ctrl E` | Go to the end of the line | As in Nano/Shell, remember as **E**nd
`Home` | Go to the beginning of line | Like every GUI text editor
`End` | Go to the end of line | Like every GUI text editor
`Ctrl Home` | Go to the beginning of the file | Like every GUI text editor
`Ctrl End` | Go to the end of the file | Like every GUI text editor 
| **Tabs** | **----------** | **----------**
`Ctrl T` | Open a new tab | Like Sublime, remember as **T**ab
`Alt L/R Arrows` | Switch between tabs. | `Ctrl Tab` cannot be mapped...
| **History** | **----------** | **----------**
`Ctrl Z` | Undo | Like Sublime
`Ctrl R` | Redo | Like no other, remember as **R**edo
| **Editing** | **----------** | **----------**
`Tab` | Indent | Like Sublime
`Shift Tab` | Unindent | Like Sublime
`Ctrl F` | Find | Like Sublime, remember as **F**Ind
`Ctrl H` | Search and Replace | Like Sublime
`Alt Up` | Move the line up | Usefull function so dedicated key (don't trust me ? Try it.)
`Alt Down` | Move the line down | Same as above             
`Ctrl K` | Delete the whole line/block | Like in nano, inspired by Sublime too, remember as **K**ill the line
`Ctrl Q` | Duplicate the line/block | Remember as "dupli**q**ate"?
`Ctrl L` | Clear/Delete all lines | Like in a shell, remember as C**l**ear
`Ctrl D` | Delete char from the left, as `Del` | Like in a shell, remember as **D**elete
`Ctrl N` | Autocomplete word | Default VIM mapping but interesting one 
| **Vital** | **----------** | **----------**
`Ctrl S` | Save | Like Sublime, remember as **S**ave
`Ctrl C` | Quit | Like in a shell
| **Miscellaneous** | **----------** | **----------**
`F2` | Set paste toggle | With paste on you can paste more easily
`F3` | Show line numbers toggle | Show or hide line numbers
`F4` | Panic Button! Toggle garbage screen | Remember as "I need to alt-**F4**!"

### Mappings in Explorer

Keys | Action | Comments
| :---: | :---: | :---: |
`Ctrl O` | Open the Explorer | Remember as **O**pen
`Enter` or `Right Arrow` | Enter a file/dir | Easy one
`Left Arrow` | Go up a dir | Easy one too
`l` | Display info on file/dir | Remember as **l**s
`n` | Open a menu to make an action (Create file/dir, Rename, Delete) | Remember as ... **N**ew action?
`a` | Toggle 'Show Hidden files only, Show All, Hide hidden files (default)' | Default mapping
`Ctrl C` | Quit | Like in a shell

### Custom commands

You can enter those command in normal mode.

Cmd | Action
| :---: | :---:
`:W` | Write the file as root
`:UndoCloseTab` | Reopen the last close buffer/tab in a new tab

## Other info

The file is **heavily** commented. You're welcome to open, read and change what you want. *It's easy.*

- Work with Vim and GVim.
- Please keep in mind that some keys **cannot** be mapped as `Ctrl Shit Something` or `Ctrl Tab` because of Terminals limitations. I have to compose with this :confused: **If you're on Windows with Putty or similar, you may experience problems because of key codes.**
- The color scheme is based on [https://github.com/sickill/vim-monokai](Monokai).
- In the bottom right-hand corner, you have three numbers `146/472-10`. Line `146`, total lines `472` and column `10`.
- Tabulations will be expanded into two spaces, the default indent size.
- UTF-8 by default.
- Backups and Swapfiles are stored in `$HOME/.vim/`.
- Pressing Enter, Space or Backspace in normal mode will enter insert mode and do action.
- When re-opening a file, Vim will remember the last position.
- When opening multiple file (as `vim file1 file2`), Vim will open those files in new tabs automatically.

## Changelog

### 1.0

Initial release.
