#   Install

* **sudo apt install gcc-arm-linux-gnueabihf**  
    安装ARM交叉编译工具
* **sudo apt install libc6-dev-i386**  
    安装ARM交叉编译工具依赖
*   **arm-linux-gnueabihf-gcc -v**  
    查看ARM交叉编译工具版本
<br>
# makefile关键字

* **$^**  
    指所有的依赖文件  
* **$<**  
    All .o files depend on the corresponding .c files   
* **＄＠**  
    refers to the target  

# gcc 编译选项
* **-g**  
    生成GDB调试信息
* **-c**  
* **-o**  
    指定编译所输出的名字



# ld 链接选项
* **-Ttext 0x80000000**  
    设置代码段起始地址

* **-o**  
    指定输出文件名字

# -objcopy 转换选项
* **-O binary**  
    指定输出为二进制文件  

* **-S**   
    不从源文件复制重定位信息和符号信息  
* **-g**  
    不从源文件复制可调试信息
<pr>

# I.MX6U infor
<pr>

* **镜像头**
 
    1. IVT (镜像向量表,就是指向程序各点的指针) 
    
    1. Boott Data (启动数据，包含镜像目标地址，镜像大小)
    2. DCD (配置信息，用于初始化一些基本的外设)




# make syntax
*   **make cmd**  
   make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf-

* **Add prefix**  
    $(addprefix fixstring,string1 string2 ...)  
* **wildcard**  
    $(wildcard *.c) means all of current directory '.c' files  
* **VPATH**   
    Example :  VPATH = src:../headers 
    Equivalent to a global path , the content of in this directory can be used everywhere
* **vpath**  
  Example : vpath  %.c  foo:bar  
　　　　　vpath  %  blish  
all of the match files  in specified directory
* **Static Pattern Rules**  
    targets .... : target-parttern : prereq-partterns...  
                    recipe  
                    ........  

* **Defining Canned Recipes**
~~~
    define v_name = 
    ...
    ....
    endef
~~~
  

*  ** The Falgs Not Pass Down by MAKEFLAGS**
~~~
            -C , -f , -o , -W
~~~


