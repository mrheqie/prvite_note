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

# make FUNCTION

* **$(subst from,to,text)**
    ~~~
    replace  "from" by "to" in text 
    ~~~
* $(patsubst pattern , replacement , text)
    ~~~
        finds whitespace-separated words in text that match pattern and replaces them with replacement
    example:
        $(patsubst  %.c , %.o  x.c.c  bar.c)
        result "x.c.o  bar.o"
     simple way:
        $(var : pattern = replacement)
        example  :
        obj = foo.o bar.o baz.o
        $(obj : .0 = .c)
        result "foo.c bar.c baz.c"
    ~~~
* $(strip string)
    ~~~
        removes leading and tailing white-space from string and replace each internal sequence of one or more whilte-space characters with a single whilte-space
        example:
            $(strip a      b c     )
            means "a b c"
    ~~~
* $(findstring find in)
    ~~~

    ~~~
* $(filter pattern... ,text)
    ~~~
    removing any words that do not match
    ~~~
* $(filter-out pattern... , text)
    ~~~
    return that do not match any of the pattern words
    ~~~

* $(sort list)
    ~~~
        Sorts the words of list in lexical order and removing duplicate words
    ~~~ 
* $(words text)
    ~~~
    return the number of words in text
    ~~~


* $(dir names....)
    ~~~
        Extracts the directory-part of each file name in names
    ~~~
* $(notdir names...)
    ~~~
        Extracts all but the dircetory-part of each file name in names
    ~~~
* $(suffix names...)
    ~~~
        Extracts the suffix of each file name in names
    ~~~
* $(basename names...)
    ~~~
    Extracts all but the suffix of each file name in names ( maybe include dir ) 
    ~~~
* $(addsuffix suffix , names...)
    ~~~
        The  value of suffix is appebded to the end of each individual name
    ~~~
* $(addprefix prefix , names....)
    ~~~
        The value of prefix is prepended to the front of each individual name
    ~~~
* $(join list1 , list2)
    ~~~
        Concaten one by one the content of  list1 and list2
    ~~~
* $(wildcard pattern)
    ~~~
    return a list of the name of existing files that match the pattern
    ~~~
* $(realpath names...)
    ~~~
    For each file name in names return the canonical absolute name
    ~~~
* $(if condition , then-part [ , else-part])
    ~~~
    if the condition is true  "then-part" evaluated and returned ,otherwise,  "else-part" evaluated and returned
    ~~~
* $(or condition1 [ , condition2 [ ,condition3...]])
    ~~~
    The first non-empty condition will be returned
    ~~~
* $(and condition1 [ , condition2 [ ,condition3...]])
    ~~~
    if one of condition is empty string then it will be returned , otherwise , return the last condition
    ~~~
* $(foreach var , list , text)
    ~~~
    Take out  the value in "list" one by one and the value of "var" is set to that value,expand the "text" ,presumably "text" contains the reference of "var",then expand the "var" in "text" 
    ~~~









  
