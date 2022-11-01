## GCC 命令格式
- `gcc [options] [filenames]` 
    - `-E 预处理，生成.i文件`
    - `-c 只编译，不链接，变成".o"`
    - `-S 生成汇编代码`
    - `-o file 把输出生成到由file指定的文件名的文件中`
    - `-g 在输出文件中加入支持调试的信息`
    - `-v verbose的意思，显示输出详细的命令执行过程信息`
## ELF
- `Linux上的core文件`也是ELF文件，在进程意外终止的时候，系统可以将该进程的部分内容和终止时的其他状态信息保存到core(核心转储文件Core Dump File)文件中
- ELF在运行时呈现以`Segement`为单位的运行视图，这个Segement中的Section的属性相同(可读可写可执行)，这样是为了节省空间，因为出错的时候是在内存中，所以是`Segment Fault`而不是`Section Fault`;而链接时，是以`Section`为单位
## Binutils
- GUN提供了一套软件来处理分析ELF文件
    - ar，归档文件，将多个文件打包成一个大文件
    - as，汇编器，将汇编文件输出为目标文件，供ld连接
    - ld，GUN链接器
    - objcopy，将目标文件的一部分或者全部内容拷贝到另外一个目标文件中，或者实现目标文件的格式转换。
    - objdump，显示ELF文件信息
    - readelf，显示更多ELF格式文件信息