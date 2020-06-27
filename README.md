# osx-terminal 美化简介 #
>虽然很多人喜欢iTerm2，我确觉得osx自带的terminal配置好了挺好用的  
>虽然美化termianl不能帮你提高编码能力，但它可以让你拥有一个好心情


## 安装powerline字体 ##
安装`Menlo Regular for Powerline` 字体，使`vim`的状态条`airline`可以显示三角形字符

>1. 从`abertsch\Menlo-for-Powerline`下载[Menlo for Powerline.ttf](https://raw.githubusercontent.com/abertsch/Menlo-for-Powerline/master/Menlo%20for%20Powerline.ttf)字体文件。(我在resource目录下也放了一份备份)
>2.  双击安装

## 安装3024 Night主题 ##
>1. 从`flemmingmiguel/osx-terminal-themes`下载[3024 Night.terminal](https://raw.githubusercontent.com/flemmingmiguel/osx-terminal-themes/master/schemes/3024%20Night.terminal)主题文件。(我在resource目录下也放了一份备份)
>2. 双击安装，并把它设置为默认
>3. 更改3024 Night主题的字体为`Menlo Regular for Powerline` 字体，字体大小18，行间距1.1
>4. 更改3024 Night主题的窗口大小为80 × 24
>5. 设置3024 Night主题，当shell退出时关闭窗口
>6. 设置默认shell为`bash`  
>`chsh -s /bin/bash`

## 配置bash ##
>1. 编辑`.bash_profile`文件，增加如下内容   
>alias ls="ls -G" 
>alias ll="ls -alGF"  
>alias grep="grep --color=auto"  
>alias ctagscxx="ctags -R --languages=c++ --langmap=c++:+..inl.c -h +..inl --c++-kinds=+px --fields=+aiSz --extra=+q"  
>export PS1='$PWD\$ '  
>export BASH\_SILENCE\_DEPRECATION\_WARNING=1


## 配置vim ##
>1. 从`VundleVim/Vundle.vim`安装`Vundle`  
>   `git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
>2. 创建vim的临时目录  
> `mkdir ~/.vimtmp`  
> `mkdir ~/.tags`  ##可以把ctags生成的标签文件放到此处，.vimrc里自动加载此处   
>  `mkdir ~/.cscope`   ##可以把cscope生成的标签文件放到此处，.vimrc里自动加载此处
>3. 从resource下载`vimrc`文件到`~/.vimrc`  
> `wget https://raw.githubusercontent.com/kdbg/osx-terminal/master/resource/vimrc -O ~/.vimrc`  
>4. 进入`vim`，执行命令下载其它插件  
>`:PluginInstall`

## 安装代码标签工具
>1. `brew install cscope`
>2. `brew install ctags`

## 效果展示 ##
![bash](https://raw.githubusercontent.com/kdbg/osx-terminal/master/image/bash.png)
![vim](https://raw.githubusercontent.com/kdbg/osx-terminal/master/image/vim.png)