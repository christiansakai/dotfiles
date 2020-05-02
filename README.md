# Dotfiles

Dotfiles configuration that aims to be as compatible (cross platform) and as performant as possible. The motivation is because I often times need to do work in my local machine but also a few other different remote machines where I can't just install binaries as I please.

The main ideas are:

- Less dependency the better because it is generally more performant and more compatible across platform
- As I gain experience using this workflow, I will strive to even cutting more dependencies
- If you must to add dependencies, consider whether it will work as compatible as possible (i.e., don't install plugins that only can use Vim8 or can only use Neovim)
- Don't be fancy, KISS

![looks](https://github.com/christiansakai/dotfiles/raw/master/looks.png "Looks")

The files and reasonings:

- `.shellrc`
    - main shell is `bash` 
    - needs to be compatible with `bash` and `zsh` since these are the most common currently
    - `starship` is used to make my prompt better without installing `zsh` and `oh-my-zsh`

- `.tmux.conf`
    - simple tmux configuration that plays well with vim

- `.minvimrc`
    - a really minimal vim configuration file
    - installed plugins are optimized only for quick editing and not full coding
    - installed plugins does not contain (or need) any external binaries
    - this is the file to be put into remote machines, butcher this file as you need

- `.vimrc`
    - a superset of the `.minvimrc` configuration
    - installed plugins for full coding experience
    - this is the file to be put into your local machines
    
- `bin/tat`
	- a helper script to launch tmux
	- run `tat` instead of `tmux`


## Basic Installation

1. Snazzy

    Color theme profile for the terminal emulator. For example, for __Terminal.app__, install [Snazzy](https://github.com/sindresorhus/terminal-snazzy). Activate the profile after the installation.

2. Powerline Fonts

    Fonts that have non-ASCII icons.

    ```sh
    $ git clone https://github.com/powerline/fonts.git --depth=1 && ./fonts/install.sh && rm -rf fonts
    ```
    
    Activate one of the Powerline fonts in your terminal after the installation.

3. Starship

    Make prompt better without installing `zsh` or `oh-my-zsh`.

    ```sh
    $ curl -fsSL https://starship.rs/install.sh | bash
    ```
	
4. Homebrew

    Mac OS package manager
    
    ```sh
    $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
    ```

5. Tmux

    Terminal multiplexer

    ```sh
    $ brew install tmux
    ```
	
6. Neovim

    Install either Neovim (and Vim-Plug)

    ```sh
    $ brew install neovim
    $ curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
    ```

    or if you can't have Neovim but have Vim preinstalled instead, then just install Vim-Plug
    
    ```sh
    curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
    ```
	
7. Activate

    Clone this repository to your `~` (which is your `$HOME`), and run these commands:

    ```sh
    $ chmod +x ~/bin/tat
    $ ln -s ~/dotfiles/.shellrc .shellrc
    $ ln -s ~/dotfiles/.tmux.conf .tmux.conf
    $ ln -s ~/dotfiles/.minvimrc .vimrc
    $ echo "source ~/.shellrc" >> .profile
    ```

    Restart your terminal. Open vim and run `:PlugInstall`.



## Extra Installation
1. Ripgrep

    Recursively search regex pattern in a directory. If this is installed, __CtrlP.vim__ and `grep` inside vim will use this instead. 

    ```sh
    $ brew install ripgrep
    ```

2. Activate

    ```sh
    $ ln -s ~/dotfiles/.vimrc .vimrc
    ```

    Open vim and run `:PlugInstall`.



## Shortcut Configuration

Nested key means that the parent key is pressed/held first before the child key.

### OSX
* Ctrl-Arrows: move between workspaces
* Cmd-Tab: move beween latest selected app
  * Arrows: move between apps
  * Opt-w: open Moom
  * Arrow: move window
  * Tab: center window
  * Space: resize to fullscreen window
  * Opt-Arrow: move and resize to halfscreen window
  * Enter: cancel window manipulation and exit Moom
  * Esc: apply window manipulation and exit Moom

### General App Navigation
* Cmd-t: new tab
* Cmd-w: delete tab
* Cmd-Opt-Arrow: move between tabs
* Ctrl-Tab: move between latest selected tab
* Cmd-f: search

### Triumvirate Environment
#### Tmux
* `tat`: start tmux the target directory
* `tmux detach`: exit from a tmux session
* `tmux attach -t [session-name]`: reattach to a tmux session
* Ctrl-d: inside tmux, this command exit and kill a tmux session
* Ctrl-q, r: reload tmux configuration
* Ctrl-q, \: split tmux pane vertically
* Ctrl-q, -: split tmux pane horizontally
* Ctrl-hjkl: move between tmux panes
* Ctrl-q, z: zoom in and out a pane
* Ctrl-q, Number: move between tabs according to the tab number
* Ctrl-q, l: move between last selected tab
* Ctrl-q, d: detach from current session
* Ctrl-q, L: move between last session
* Ctrl-q, [: enter copy mode
  * v: Start selection in copy mode
  * y: copy to clipboard
  * Enter: exit copy mode
* Trackpad/Mouse scroll: you can scroll (the same as copy mode) also using a Trackpad/Mouse
* Ctrl-d, exit a pane
* Ctrl-q, b: break current split pane to a new tab
* Ctrl-q, c: new tab
* Ctrl-q, j: join pane from x to current window
* Ctrl-q, s: swap a pane
* Ctrl-s: forward incremental search
* Ctrl-r: backaward incremental search
* Ctrl-q, Space: swap panes

#### Vim
* `vi`, or `vim`, or `nvim`: start neovim
* Ctrl-p: fuzzy file finder
  - Ctrl-k: move up result
  - Ctrl-j: move down result
  - Ctrl-t: open selected file on a new tab
  - Ctrl-s: open selected file on a split pane
  - Ctrl-v: open selected file on a vertical split pane
  - Ctrl-c: exit fuzzy file finder
* Ctrl-n: toggle tree file viewer
* Ctrl-f: prettify JS/HTML/CSS
  - %: create new file
  - d: create new directory
  - R: rename directory
  - D: delete directory
* Space-vi: open .vimrc on a new tab
* Space-so: source .vimrc
* Ctrl-y ,: emmet.io style html css expand
* Ctrl-w, Shift-HJKL: move a pane to another location
* Ctrl-w, << or >>: increase a pane size
* Space, or: open a runner
* Space, nr: open a node interactive runner
* Space, kr: kill a runner
* Space, sc: send command to runner
* Space, cr: clear runner
* Space, sf: send the current file to be executed to a runner
* Fn-F1: go into vim help, also helpful if you are stuck in Insert(paste) mode, then do `:set nopaste` to get out of that
* `:%s/replacewith/this`: to search and replace on one file
* `:%1,99s/replacewith/this`: to search and replace from one line number to another line number
* `:s/replacewith/this`: to search and replace text within visual block mode
* To search and replace across files
  * `:args **/*.sample_file.js`
  * `:argdo %s/replacewith/this/ge | update`
* To search files that contain a word
  * `:grep! "my word" path/to/file/**/*.js` and then upon new window type `:cw command`
  * or just press K (uppercase K) on top of a word
* To search files that contains a word using regex
  * `:grep! "^export\sdefault" path/to/file/**/*.js` and then upon new window type `:cw command`
* To autocomplete
  * Autocomplete works with pressing Tab to select the completion
* Normal Mode:
  * Ctrl-s: save file
  * Ctrl-u: previous page
  * Ctrl-d: next page
  * gt: next tab 
  * gT: previous tab
  * Ctrl-w, Shift-t: break current window to a new tab
  * Space--: zoom in a pane
  * Space-=: rebalance pane
* Insert Mode:
  * Ctrl-s: exit insert mode to normal mode
* Visual Mode:
  * Ctrl-s: exit visual mode to normal mode
  * Shift-i: append before a character
  * Shift-a: append after a character
  * y: yank (copy) to system clipboard


## Todo

- Think of a way to avoid duplication on `.minvimrc` and `.vimrc`
