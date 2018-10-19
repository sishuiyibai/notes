### Vundle安装
1. 下载原码包到本地~/.vim/bundle/下，如该路径目录不存在，mkdir创建出来

        $ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
2. 更新(创建)~/.vimrc配置文件
> 添加以下配置模版代码，并按需删减/增添插件配置项:

         set nocompatible              " be iMproved, required
	     filetype off                  " required
	     " set the runtime path to include Vundle and initialize
	     set rtp+=~/.vim/bundle/Vundle.vim
	     call vundle#begin()
	     " alternatively, pass a path where Vundle should install plugins
	     "call vundle#begin('~/some/path/here')
	     " let Vundle manage Vundle, required
	     Plugin 'VundleVim/Vundle.vim'
	     " The following are examples of different formats supported.
	     " Keep Plugin commands between vundle#begin/end.
	     " plugin on GitHub repo
	     Plugin 'tpope/vim-fugitive'
	     " plugin from http://vim-scripts.org/vim/scripts.html
	     " Plugin 'L9'
	     " Git plugin not hosted on GitHub
	     Plugin 'git://git.wincent.com/command-t.git'
	     " git repos on your local machine (i.e. when working on your own plugin)
	     Plugin 'file:///home/gmarik/path/to/plugin'
	     " The sparkup vim script is in a subdirectory of this repo called vim.
	     " Pass the path to set the runtimepath properly.
	     Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
	     " Install L9 and avoid a Naming conflict if you've already installed a
	     " different version somewhere else.
	     " Plugin 'ascenator/L9', {'name': 'newL9'}
	     " All of your Plugins must be added before the following line
	     call vundle#end()            " required
	     filetype plugin indent on    " required
	     " To ignore plugin indent changes, instead use:
	     "filetype plugin on
	     " Brief help
	     " :PluginList       - lists configured plugins
	     " :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
	     " :PluginSearch foo - searches for foo; append `!` to refresh local cache
	     " :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
	     " see :h vundle for more details or wiki for FAQ
	     " Put your non-Plugin stuff after this line
> 详情请查看github官方文档：
> > https://github.com/VundleVim/Vundle.vim#people-using-vundle
3. 安装插件命令：
>方法1: 终端打开vim，运行:PluginInstall命令

>方法2：命令行输入：vim +PluginInstall +qall
4. 为使用fish shell,将`set shell=/bin/bash`添加入你的.vimrc文件中。
