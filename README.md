## vim-settings for *vim-python-ide*
*vim-python-ide* provides bundled plugins to transform your *vim* editor into useful and comfortable python ide.
### Requirements
In order to use this you should have already installed:
* [vim editor](http://vim.org)
* [git](https://git-scm.com)
* [vundle](https://github.com/VundleVim/Vundle.vim.git)
* [Powerline Fonts](https://github.com/powerline/fonts)

### Installation
#### * Install git and vim
If you are running linux, most probably you will already have *vim* and *git* installed. As there is a great flavour of linux with different package management systems, this packages installation will not be discussed.
#### * Install *vim-settings*
This task conludes in two basic steps - download "vim-settings" and "copy" to your *.vimrc* file. It is always good idea to keep your previous settings backed up, so:
```
$ git clone https://github.com/yyovkov/vim-settings /tmp/vim-settings
$ cp ~/.vimrc ~/.orig-vimrc
$ cp ~/vim-settings/vimrc-python-ide ~/.vimrc
```
Consider deleting of the directory: */tmp/vim-settings*.
#### * Install [Powerline Fonts](https://github.com/powerline/fonts)
*Powerline Fonst* installation is quite simple and is well described in details on github page of the project. However I'm repeating the commands here in order simplify *vim-settings* installation:
```
$ git clone https://github.com/powerline/fonts /tmp/powerline_fonts
$ cd /tmp/powerline_fonts
$ ./install.sh
```
Consider deletion of the directory */tmp/powerline_fonts*.
#### * Install [vundle](https://github.com/VundleVim/Vundle.vim.git)
It is supposed vundle to be already installed, however this is a single command, that can be read from the project github page, so I am adding this command here in order to minimize ones browsing different pages in internet. The command is:
```
$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
$ vim +InstallPlugin +qall
```

### CLI Configuration
*vimrc-python-ide* provides bundled plugins working in *GUI* version of VIM. In order to use this settings in *CLI* (Command Line Interface) like gnome-terminal or konsole, or even in linux text-only mode, the following should be done:
#### Setup terminal fonts
Set the fonts of your terminal to one of your choice, provided by "Powerline fonts" from steps above. You will easy determine this fonts, as their names ends with "*Powerline*". As the terminals settings vary on different terminal, refer to your terminal documentation to do that. 
#### Update *vimrc-python-ide*
The way *GUI* settings are distringuished from *CLI* ones is a "*if*" clouse. So commenting out "start" and "end" of that clause will do the job. As there are numerious "*if*"'s, *vimrc-python-ide* has idented the "*GUI*" section of file for better readability. So, let's do some work and comment out lines:
```
5 " if has("gui_running") "Start of pluggins IF
```
and 
```
89 " endif " End of plugins IF
```
