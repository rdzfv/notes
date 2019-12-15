##文件夹和文件操作
###文件操作
**文件复制：**
命令格式：`cp [-adfilprsu] 源文件(source) 目标文件(destination)`
`cp [option] source1 source2 source3 ... directory`
>参数说明：
-a:是指archive的意思，也说是指复制所有的目录
-d:若源文件为连接文件(link file)，则复制连接文件属性而非文件本身
-f:强制(force)，若有重复或其它疑问时，不会询问用户，而强制复制
-i:若目标文件(destination)已存在，在覆盖时会先询问是否真的操作
-l:建立硬连接(hard link)的连接文件，而非复制文件本身
-p:与文件的属性一起复制，而非使用默认属性
-r:递归复制，用于目录的复制操作
-s:复制成符号连接文件(symbolic link)，即“快捷方式”文件
-u:若目标文件比源文件旧，更新目标文件 


如将/test1目录下的file1复制到/test3目录，并将文件名改为file2,可输入以下命令：
`cp /test1/file1 /test3/file2`

**文件移动：**
命令格式：`mv [-fiv] source destination`
>参数说明：
-f:force，强制直接移动而不询问
-i:若目标文件(destination)已经存在，就会询问是否覆盖
-u:若目标文件已经存在，且源文件比较新，才会更新

如将/test1目录下的file1复制到/test3 目录，并将文件名改为file2,可输入以下命令：
`mv /test1/file1 /test3/file2`


**文件删除命令**
命令格式：`rm [fir] 文件或目录`
>参数说明：
-f:强制删除
-i:交互模式，在删除前询问用户是否操作
-r:递归删除，常用在目录的删除

如删除/test目录下的file1文件，可以输入以下命令：
`rm -i /test/file1`
<br>

### 文件夹操作
###删除文件夹
>-r 就是向下递归，不管有多少级目录，一并删除
-f 就是直接强行删除，不作任何提示的意思

`rm -rf 文件路径、文件名` &nbsp; 会删除目录下的所有文件和文件夹
<br> 


##进程和端口
**已知端口号，查看占用其的进程** &nbsp; `netstat -lnp|grep 端口号`
**查看某进程占用的端口** &nbsp; `ps -ef|grep 进程名` &nbsp; 举例nginx `ps -ef|grep nginx`
