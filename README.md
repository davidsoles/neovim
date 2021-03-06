<h1 align="center"> ✨ Vim/Neovim Configuration ✨ </h1>

## Introduction
This repository holds the necesary files to configure Neovim as a text editor.

## Prerequisites
- Neovim 0.5 or higher (can be installed using **brew**)
- FZF (can be installed using **brew**)
- FD (can be installed using **brew**)
- RipGrep (can be installed using **brew**)

## Plugin Manager
A minimalist Vim Plugin Manager. More info [here](https://github.com/junegunn/vim-plug).

## Basic Plugins
- Plug 'airblade/vim-gitgutter'
- Plug 'arcticicestudio/nord-vim'
- Plug 'doums/darcula'
- Plug 'dracula/vim', { 'as': 'dracula' }
- Plug 'github/copilot.vim'
- Plug 'gruvbox-community/gruvbox'
- Plug 'iamcco/markdown-preview.nvim', { 'do': 'cd app && yarn install' }
- Plug 'itchyny/lightline.vim'
- Plug 'jiangmiao/auto-pairs'
- Plug 'josa42/vim-lightline-coc'
- Plug 'junegunn/fzf'
- Plug 'junegunn/fzf.vim'
- Plug 'neoclide/coc.nvim', {'branch': 'release'}
- Plug 'preservim/nerdtree'
- Plug 'puremourning/vimspector'
- Plug 'rust-lang/rust.vim'
- Plug 'stsewd/fzf-checkout.vim'
- Plug 'tpope/vim-commentary'
- Plug 'tpope/vim-fugitive'
- Plug 'vim-syntastic/syntastic'

## Conquer of Completion (CoC)
Conquer of completion is a pluging that autoconfigure many Language Server Protocols (LSP) such as Javascript, Rust, Golang and Java among others, making the larning curve for new users of Neovim so much easier. More info [here](https://github.com/neoclide/coc.nvim).

## CoC Extensions
This is a list of CoC Extensions used during the installation. More info [here](https://github.com/neoclide/coc.nvim/wiki/Using-coc-extensions).
- coc-angular
- coc-go
- coc-html
- coc-java
- coc-java-vimspector
- coc-json
- coc-rust-analyzer
- coc-toml
- coc-tsserver
- coc-yaml

## Fuzzy Finder (fzf)
Is a general purpose command line fizzy finder. The configuration can be set in multiple files but in this case we are going to put it in .zshrc file at the home folder. More info [here](https://github.com/junegunn/fzf).

```bash
export FZF_DEFAULT_COMMAND="fd --type f --type l --follow --exclude={.m2,.git,.idea,.vscode,node_modules,target,'*.class'}"
```

It is posible to change the fuzzy finder background color selector and pointer. More info [here](https://github.com/junegunn/fzf/issues/1602#issuecomment-511663634).

```bash
export FZF_DEFAULT_OPTS="$FZF_DEFAULT_OPTS --color=bg+:#3B4252,bg:#2E3440,spinner:#81A1C1,hl:#616E88,fg:#D8DEE9,header:#616E88,info:#81A1C1,pointer:#81A1C1,marker:#81A1C1,fg+:#D8DEE9,prompt:#81A1C1,hl+:#81A1C1"
```

## Rest In Peace Grep
Is a line-oriented search tool that recursively searches the current directory for a regex pattern. More info [here](https://github.com/BurntSushi/ripgrep).

## Syntastic
Syntastic is a syntax checking plugin for Vim created by Martin Grenfell. It runs files through external syntax checkers and displays any resulting errors to the user. This can be done on demand, or automatically as files are saved. More info [here](https://github.com/vim-syntastic/syntastic).

This environment variable is use to set the repository location that contains the files needed for Syntastic to work.

```bash
export SYNTASTIC_JAVA_CLASSPATH="$HOME/.config/syntastic"
```

This plugins needs to use Java [Checkstyle Library](https://github.com/checkstyle/checkstyle/releases/) and the XML file with the coding standards that are going to be verified. The following [XML](https://gist.githubusercontent.com/davidsoles/86f9a454cdde53f0450b80cba856efe4/raw/12782c4995de44046aee4659b8fdaeb7d676cf5c/CheckstyleConfigurationUrbe.xml) file was prepared by David Soles and represents an example of what can be achieve using this tool.
