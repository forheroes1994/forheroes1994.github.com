Linux基本命令

ls　　        显示文件或目录

     -l（-list）   列出文件详细信息内容   格式：ls [-l]<目录名>   

     -a          列出当前目录下所有文件及目录，包括隐藏的文件    格式：ls [-a]<目录名>   

mkdir         创建目录  格式：mkdir [参数]<目录名> 

     -p          创建多级目录，若无父目录，则创建p  

rmkdir        删除空目录  

rm              删除文件  

    -f            强制删除

    -rf 　　  递归强制删除　　　

cd              切换目录   格式：<相对路径/绝对路径>  //相对路径指从当前路径开始的路径，绝对路径指是从盘符开始的路径。

touch         创建空文件  格式：touch[参数]<文件名>

cat             标准输出查看文件内容 格式：cat[参数] <文件名>

cp              拷贝   格式：cp[参数]<源文件或目录>　<目标路径文件或目录>

    -r　　    递归复制文件夹

mv            移动或重命名  格式：cp[参数]<源文件或目录>　<目标路径文件或目录>

find           在给定位置搜索与条件匹配的文件 格式：find[路径][参数] <文件名>   

eg：1.   #find .-name 'main*'  //查找当前目录中以“main”开头的文件     2.  #find .-name 'tmp' -xtype c -user 'zch'  //查找当前目录下文件名为'tmp' 文件类型为c 用户名为zch的文件

  -name　 区分大小写

  -iname　不区分大小写

wc            统计文本中行数、字数、字符数  格式：wc[选项]<文件名>

     -c 　　统计字符数

     -w　　 统计单词数

     -l　      统计行数

grep         在文本文件中查找某个字符串  格式：grep[参数]<文件名>

pwd          显示当前目录

du            查看目录大小 du -h /home带有单位显示目录信息  格式：du [选项]<文件>  

    -a         显示目录中个别文件的大小。   

    -b         显示目录或文件大小时，以byte为单位

    -s         显示总计，只列出最后加总的值。

df　　　 查看磁盘使用情况   格式：df [参数] <文件>

ps　　　查看目前程序运行情况  格式：ps [options] [--help]

   -a        列出所有的进程

   -au     显示较详细的资讯

  -aux     查看没有中断的应用程序

kill　　  杀死进程。//先用ps 或 top命令查看进程的id，然后再用kill命令杀死进程。 格式：kill[参数][进程号]

   -l　　 列出所有信号名称

free　　 简洁的查看系统内存使用情况

    -m      以M为单位查看内存使用情况（默认为kb）

    -b       以字节为单位查看内存使用情况

top　　  实时的对系统处理器的状态监视

grep　　用于过滤/搜索的特定字符，使用正则表达式搜索文本并打印   格式：grep [参数] 文件名1，文件名2，...，文件名n

    -i        不区分大小写（单字符）

    -l        只输出文件名（多文件时）

    -v       显示不包含匹配文本的所有行

    -n      显示匹配行及行号

a）查看文件大小、内存大小、cpu信息、硬盘空间

查看文件大小：ls 、du 　　内存大小 ：free 、top、htop　htop的使用参考：http://blog.csdn.net/skh2015java/article/details/53173896

硬盘空间：df 　　//df命令的使用参考：http://www.cnblogs.com/peida/archive/2012/12/07/2806483.html

b)查看目前运行程序情况，剩余内存，kill程序

 查看目前运行程序情况：htop、top、ps　　剩余内存：free //   total=used+free    实际内存占用：used-buffers-cached 即 total-free-buffers-cached    实际可用内存：buffers+cached+free

kill程序：kill、kill -9 pid

c）sed命令与grep命令使用参考：http://www.cnblogs.com/52fhy/p/5836429.html