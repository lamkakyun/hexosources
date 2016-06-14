---
title: 我的vimrc配置文件
date: 2016-06-14 23:32:51
tags:
  - vim
---

``` bash
""""""""""""""""""""""""""""""""""""""""
" vundle plugin configuration
""""""""""""""""""""""""""""""""""""""""
set nocompatible            
filetype off
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'gmarik/Vundle.vim'

Plugin 'Shougo/neocomplete.vim'
Plugin 'ervandew/supertab'
Plugin 'tristen/vim-sparkup'
Plugin 'tpope/vim-commentary'
Plugin 'scrooloose/syntastic'
Plugin 'scrooloose/nerdtree'
Plugin 'jiangmiao/auto-pairs'
Plugin 'vim-scripts/taglist.vim'
Plugin 'shawncplus/phpcomplete.vim'

call vundle#end()        
filetype plugin indent on
""""""""""""""""""""""""""""""""""""""""
" jet 简单配置
""""""""""""""""""""""""""""""""""""""""
syntax on
set nocompatible
set history=1000
set nu
highlight StatusLine guifg=SlateBlue guibg=Yellow
highlight StatusLineNC guifg=Gray guibg=White
set nobackup
setlocal noswapfile
set ruler
set rulerformat=%20(%2*%<%f%=\ %m%r\ %3l\ %c\ %p%%%)
set cmdheight=2
set backspace=2
set showmatch
set ignorecase
set hlsearch
set incsearch
set statusline=%F%m%r%h%w\[POS=%l,%v][%p%%]\%{strftime(\"%d/%m/%y\ -\ %H:%M\")}
set laststatus=2
set tabstop=4
set softtabstop=4
set shiftwidth=4
""""""""""""""""""""""""""""""""""""""""
" 配置按键
""""""""""""""""""""""""""""""""""""""""
map <Left> <None><CR>
map <Right> <None><CR>
map <Up> <None><CR>
map <Down> <None><CR>
""""""""""""""""""""""""""""""""""""""""
" NERDTree配置
""""""""""""""""""""""""""""""""""""""""
map <C-n> :NERDTreeToggle<CR> " 有了supertab，就不需要这个按键了

"""""""""""""""""""""""""""""""""""""""""
" taglist 配置
""""""""""""""""""""""""""""""""""""""""
let Tlist_Use_Right_Window = 1   " 右侧打开
let Tlist_Ctags_Cmd = '/usr/bin/ctags'
let Tlist_Exit_OnlyWindow = 1  " 如果taglist窗口是最后一个窗口，则退出vim"
let Tlist_Show_One_File = 1   " 不同时显示多个文件的tag，只显示当前文件的"
map <silent> <F9> :TlistOpen<cr>

```
