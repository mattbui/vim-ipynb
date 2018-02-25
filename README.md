# vimpyter

<p align="center">
  <img src="https://github.com/vyzyv/vimpyter/blob/master/images/jupyter_logo.png" height=200/> 
  <img src="https://github.com/vyzyv/vimpyter/blob/master/images/vim_logo.png" width=200/>
</p>

**Edit Jupyter notebooks in your favourite editor (yeah, vim or neovim)**

## Demo

## Installation

To install this plugin you should use plugin manager like **[vim-plug](https://github.com/junegunn/vim-plug)** or **[Vundle](https://github.com/VundleVim/Vundle.vim)**:

```vim
Plug 'vyzyv/vimpyter' "vim-plug
Plugin 'vyzyv/vimpyter' "Vundle
```

If you want to use different plugin manager/direct instalation please do refer to their respective repositories/documentation.

**Make sure you have the required dependencies**

## Dependencies

- **Vim8 with asynchronous support or neovim**
- **[notedown](https://github.com/aaren/notedown)**

## Configuration

Plugin provides some convenience commands:

  - **VimpyterStartJupyter**: asynchronously starts [jupyter notebook](http://jupyter.org) instance from Vim/Neovim
  - **VimpyterStartNteract**: asynchronously starts [nteract](https://github.com/nteract/nteract) instance from Vim/Neovim
  - **VimpyterInsertPythonBlock**: inserts block of python code (see Demo)

Example mappings (**put this in your .vimrc/init.vim**):

```vim
autocmd Filetype jupyter nmap <silent><Leader>b :VimpyterInsertPythonBlock<CR>
autocmd Filetype jupyter nmap <silent><Leader>j :VimpyterStartJupyter<CR>
autocmd Filetype jupyter nmap <silent><Leader>n :VimpyterStartNteract<CR>
```

## Integrations with other plugins

Currently supported plugins:

- [w0rp/ale](https://github.com/w0rp/ale): asynchronous linter and fixer for Vim/Neovim
- [Shougo/deoplete](https://github.com/Shougo/deoplete.nvim): asynchronous completion framework for Vim/Neovim

You can request additional integrations or create them on your own (**pull requests are welcomed**)

## Known bugs

- [nteract crashes on startup](https://github.com/nteract/nteract/issues/2582#issuecomment-368308596)

If you find a bug please post an issue.


