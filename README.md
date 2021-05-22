# vimrc-bynmboy
this is my vimrc setup, whith plugins, colorscheme and more

my channel on youtube ( portuguese language ):
youtube.com/fabiocarneiro

my website ( portuguese language );
www.fabioaacarneiro.com.br

my gruvbox theme for xterm terminal emulator:
https://github.com/bynmboy/gruvbox-xterm

my e-mail for contact:
fabiocarneiro@slackjeff.com.br

nvim deepin 20 whitout colorscheme

![Alt text](https://github.com/bynmboy/vimrc-bynmboy/blob/master/vim.png)


gvim windows seven with gruvbox light colorscheme

![Alt text](https://github.com/bynmboy/vimrc-bynmboy/blob/master/gvim.PNG)


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

for slackware users this python 3.7 from my repository on google drive:

https://drive.google.com/drive/u/2/folders/1oZDT1yxhozkJKWwSNB76uO89LyciA7Je

maybe in linux for nvim users, for activated python support
you need run with pip3

pip3 install --user nvim
or in case some plugins don't work because they need python integration with
vim or neovim, you need run the following commands

in case you use neovim:
pip3 install pynvim

in case you use vim:
pip3 install pyvim

after this step, run in nvim 

:checkhealth 

for check the python support in your nvim
in vim case, you don't need do this, just
install VimPlug to install the plugins in
my vimrc

to install vimplug, follow the instruction on link bellow:
https://github.com/junegunn/vim-plug

after vimplug installed with success open your vim or nvim
and run command bellow:

:PlugInstall

after all plugins has succesfully installed
use Ctrl+w, q  to close dialog of plugin install in editor
close and reopen your editor or try use command bellow:

for vim
:source ~/.vimrc

for neovim
:source ~/.config/nvim/init.vim

on windows, location of vimrc file is diferent to find,
where file is locate use in vim or neovim the bellow command
on your vim or neovim

:echo $MYVIMRC

now you know how find your vimrc file or init.vimrc file

chocolatey:
https://chocolatey.org/

powershell:
https://docs.microsoft.com/pt-br/powershell/?view=powershell-7

neovim:
https://neovim.io/

vimawesome ( lot of plug for vim ):
vimawesome.com/

vim-plug:
https://github.com/junegunn/vim-plug

vim:
https://www.vim.org/download.php

case you use Debian, or other Debian-based distro, vim in debian repo
don't have python3 support, you can check this whith bellow command
:echo has("python3")
if this command return 0, your vim don't have python support,
case return 1, your vim have support for python

you have 3 choise to resolve this problem:
1 compile the vim whith python suport, but is more dificult
and i recomend bellow 2 options:
use vim-gtk,but if you don't like gtk application go to
the last solution, use neovim, he coming whith python support,
this is more easy.

for Windows user, you need download vimrc-windows and rename 
to use on vim (_vimrc) or nvim (init.vim)

for linux user, you need download vimrc-linux and rename to
use on vim (.vimrc) or nvim (init.vim)

if you are web developer, and if are you need use live server, you need configure Bracey correctly,
in vimrc file Bracey is configured to start when you open HTML files
but, you need nodejs installed on you system, i don't test this on windows
but on linux it's super easy, just follow the commands bellow:

you need go to plugin directory, the command bellow it's for vim plug, thats it's exacly what
we use in this repository:

1- cd ~/.vim/plugged/bracey.vim for plug
2- run npm install --prefix server

*** the numbers 1 and 2 it's just for show you like a list like "how to do" alright ? kkk ***

you can automate this for vim-plug by using the following command in your .vimrc:

Plug 'turbio/bracey.vim', {'do': 'npm install --prefix server'}. 

This will run the npm command every time you update the plugin as well
in case you use neovim, you need adaptade this command for you

vim on live-server:
![Alt text](https://github.com/bynmboy/vimrc-bynmboy/blob/master/gitpic.png)

![Alt text](https://github.com/bynmboy/vimrc-bynmboy/blob/master/vimfile.png)


