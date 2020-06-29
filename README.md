# vimrc-bynmboy
this is my vimrc setup, whith plugins, colorscheme and more

my channel on youtube ( portuguese language ):
youtube.com/fabiocarneiro

my gruvbox theme for xterm terminal emulator:
https://github.com/bynmboy/gruvbox-xterm

my e-mail for contact:
fabiocarneiro@slackjeff.com.br

this setup you can programing in various languages whith autocomplete
omnifunc, show syntax errors, snippets, all you need to programing like a boss on vim

remember, you can use this setup whith vim, neovim, gvim ( or vim-gtk )
running in windows, linux or mac, but you need other more things like:
python 3.7, git,vim-plug, etc. In windows Seven, i need powershell,
chocolatey and gvim for better experience in my works whith vim.
In linux you don't need some things, i gues this things has instaled on distro,
in my Slackware i'dont need install nothing, just only vim-plug.In Mac, 
i don't know if you are need install something to use well this setup, 
i never has use mac xD. Windows 8 or 10, just install Chocolatey in Power-Sell and
use " choco install 'program' ". I will past in here somes link case you need ther.

python:
https://www.python.org/
maybe in linux for nvim users, for activated python support
you need run with pip3
pip3 install --user nvim
after this step, run in nvim " :checkhealth " for check the
python support in your nvim

chocolatey:
https://chocolatey.org/

powershell:
https://docs.microsoft.com/pt-br/powershell/?view=powershell-7

vim:
https://www.vim.org/download.php

neovim:
https://neovim.io/

vimawesome ( lot of plug for vim ):
vimawesome.com/

vim-plug:
https://github.com/junegunn/vim-plug

for Windows user, just copy all code bellow and, paste this code in
yout .vimrc or init.vim, or _vimrc, this file name depend if you use linux or windows

" Vim with all enhancements
source $VIMRUNTIME/vimrc_example.vim

" Use the internal diff if available.
" Otherwise use the special 'diffexpr' for Windows.
if &diffopt !~# 'internal'
  set diffexpr=MyDiff()
endif
function MyDiff()
  let opt = '-a --binary '
  if &diffopt =~ 'icase' | let opt = opt . '-i ' | endif
  if &diffopt =~ 'iwhite' | let opt = opt . '-b ' | endif
  let arg1 = v:fname_in
  if arg1 =~ ' ' | let arg1 = '"' . arg1 . '"' | endif
  let arg1 = substitute(arg1, '!', '\!', 'g')
  let arg2 = v:fname_new
  if arg2 =~ ' ' | let arg2 = '"' . arg2 . '"' | endif
  let arg2 = substitute(arg2, '!', '\!', 'g')
  let arg3 = v:fname_out
  if arg3 =~ ' ' | let arg3 = '"' . arg3 . '"' | endif
  let arg3 = substitute(arg3, '!', '\!', 'g')
  if $VIMRUNTIME =~ ' '
    if &sh =~ '\<cmd'
      if empty(&shellxquote)
        let l:shxq_sav = ''
        set shellxquote&
      endif
      let cmd = '"' . $VIMRUNTIME . '\diff"'
    else
      let cmd = substitute($VIMRUNTIME, ' ', '" ', '') . '\diff"'
    endif
  else
    let cmd = $VIMRUNTIME . '\diff'
  endif
  let cmd = substitute(cmd, '!', '\!', 'g')
  silent execute '!' . cmd . ' ' . opt . arg1 . ' ' . arg2 . ' > ' . arg3
  if exists('l:shxq_sav')
    let &shellxquote=l:shxq_sav
  endif
endfunction
"linux user, copy the code bellow, you don't
"need more then this, 
call plug#begin()
Plug 'morhetz/gruvbox'
Plug 'scrooloose/nerdtree'
Plug 'sirver/ultisnips'
Plug 'honza/vim-snippets'
Plug 'ervandew/supertab'
Plug 'w0rp/ale'
Plug 'sheerun/vim-polyglot'
Plug 'shougo/neocomplete.vim'
Plug 'jiangmiao/auto-pairs'
Plug 'vim-scripts/AutoComplPop'
Plug 'vim-test/vim-test'
call plug#end()

" for better font to use on windows discoment line bellow
"set guifont=Lucida_Console:h14:cANSI:qDRAFT
set relativenumber
set title
set background=light
set tabstop=4 softtabstop=4 shiftwidth=4 noexpandtab
colorscheme gruvbox

let g:UltiSnipsJumpForwardTrigger="<TAB>"
let g:UltiSnipsJumpBackwardTrigger="<S-TAB>"
let g:UltiSnipsEditSplit="vertical"
let g:SuperTabDefaultCompletionType = "<c-n>"

map <F2> :NERDTreeToggle <CR>
map <F3> :!javac "%" && java "%" <CR>
map <F4> :!luac "%" && lua "%" <CR>
"command bellow open cmd windows, change for your terminal linux
nnoremap <C-t> :!cmd <CR>
" save command whith Ctrl + s
nnoremap <C-s> :w! <CR>
" save command whith s
nnoremap <s> :w <CR>
" save command whith Ctrl + q
nnoremap <C-q> :q! <CR>
" save command which q
nnoremap <q> :q <CR>
  
" in GVim on windows or linux to open explorer or file manager 
" to open a file whith " Ctrl + o " discoment line bellow
"nnoremap <C-o> :browse open <CR>
  
" in Gvim on windows or linux to open explorer or file manager 
" to open 'save as' explorer whith " Ctrl + s " discoment line bellow
"nnoremap <C-s> :browse save <CR>
