# 常用的部分linux命令

这里只展示部分常用命令，命令也只展示部分常用选项



## man 查看指令文档手册

`man [option] [name]`

E.g.

`man man`

`man ls`

`man git`

> 当要导出内容的时候，比如 `man tree > tree.txt` 时，查看内容混乱或者乱码。
>
> 解决方法: 再加入`col -b`操作
>
> E.g.  `tree man | col -b > tree.text`





## ls 展示目录文件

`ls [option] [path]`

**option**

+ `-a` 显示隐藏文件
+ `-l` 显示详细信息

E.g.

`ls -l`

`ls -la /usr/local`



## pwd 查看当前工作目录

`pwd [option]`

**option**

+ `-L` 显示当前逻辑工作目录
+ `-P` 显示当前物理工作目录



## cd 跳转/切换工作目录

`cd`

E.g.

`cd ~/Desktop`  跳转到当前用户的Desktop文件夹



## cp 复制文件

`cp [sourceFile] [targetFile]`

E.g.

`cp t1.txt text/` 将当前目录的t1.txt文件复制到当前目录text文件夹内

`cp t1.txt text/t2.txt` 将当前目录的t1.txt文件复制到当前目录text文件夹内并改为t2.txt

`cp /home/me/t1.txt /usr/` 使用绝对目录，将/home/me/t1.txt文件移动到/usr/目录下



## mv 移动文件

`mv [sourceFile] [targetFile]`

E.g.

`mv t1.txt text/` 将当前目录的t1.txt文件移动到当前目录text文件夹内

`mv t1.txt text/t2.txt` 将当前目录的t1.txt文件移动到当前目录text文件夹内并改为t2.txt

`mv /home/me/t1.txt /usr/` 使用绝对目录，将/home/me/t1.txt文件移动到/usr/目录下



## mkdir 新建文件夹

`mkdir [directory]`

E.g.

`mkdir /home/myfolder` 在/home路径下创建myfolder文件夹



## col 过滤控制字符

在使用`>` 或者 `>>` 输出到内容文件时候，多余的控制字符会导致内容乱码，`col` 命令能过滤这些字符

`col [option]`

**option**

+ `-b` 过滤掉所有控制字符，包括RLF和HRLF
+ `-f` 过滤RLF字符
+ `-x` 过滤以多个空格表示跳格的字符
+ `-l<缓冲区列数>` 预设的内存缓冲区有128列，用户可以自行指定缓冲区的大小

