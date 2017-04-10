Esc : prepare for new commands.

i : insert mode, you can write and delete text in this mode.

a : append mode, similar to the insert mode but it moves the cursor to the next location.

^ : go to the beginning of the line.

$ : go to the end of the line

/hello  : find “hello” in the file (then you can use n and N for next and previous occurences)

:34  : go to line “34”

G : go to the last line

dd : delete line

5dd : delete five lines beginning from the cursors line.

yy : (yank) copy line

p : paste

5yy : (yank) copy five lines beginning from the cursors line.

u : undo

w : save modifications

q : quit without saving

wq : save and quit

q! : quit without saving

V : select lines (you can use the arrows to select more or less lines)

v : select characters (you can use the arrows to select more or less lines)

:set number : show lines’ numbers


# vim
1 /etc/vim/vimrc 是所有用户的配置，~/.vimrc只影响到单个用户。
2 /usr/share/vim/vimrc是/etc/vim/vimrc的一个硬链接（$ ll /usr/share/vim/vimrc 就可以看到），一般只修改~/.vimrc就行了。colors,plugins,docs都是在VIMRUNTIME目录下的，你可以先在vim的命令模式下输入:echo $VIMRUNTIME（如果没有自己另行修改，一般是/usr/share/vim/vim7x）,然后把你下载的molokai.vim复制到下面的colors文件夹里。
3 切换颜色方案:colorscheme molokai(only for once),也可以添加到.vimrc里(every time)，要退出重启后才生效。

Download [plug.vim] https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim and put it in ~/.vim/autoload 
