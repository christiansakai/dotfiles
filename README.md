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
    - this needs to be separated into smaller configurations because inside there is a fzf

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


## Basic Requirements
### Install Basic Software

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
	
5. Neovim

	Install either Neovim (and Vim-Plug)

	```sh
	$ brew install neovim
	$ curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
	```
	
	or if you can't have Neovim but have Vim preinstalled instead, then just install Vim-Plug
	
	```sh
	curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
	```
	

### Activate

Clone this repository to your `~` (which is your `$HOME`), and run these commands:

```sh
$ chmod +x ~/bin/tat
$ ln -s ~/dotfiles/.shellrc .shellrc
$ ln -s ~/dotfiles/.tmux.conf .tmux.conf
$ echo "source ~/.shellrc" >> .profile
```

If you want to use a very simple Vim setup for your remote machine

```sh
$ ln -s ~/dotfiles/.minvimrc .vimrc
```

If you want to use a more through Vim setup

```sh
$ ln -s ~/dotfiles/.vimrc .vimrc
```

Restart your terminal. Open vim and run `:PlugInstall`


### Install Extra Software
1. Ripgrep

    Recursively search regex pattern in a directory. If this is installed, __CtrlP.vim__ and `grep` inside vim will use this instead. 

    ```sh
    $ brew install ripgrep
    ```


## Todo

- Think of a way to avoid duplication on `.minvimrc` and `.vimrc`
- Add cheatsheet
