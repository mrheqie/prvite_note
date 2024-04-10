# vim
	- ## learnin notes
	- ### cmd mode
		- del single char : x
		- del single line : dd
		- cpy single line : yy
		- paste data      : p
		- left move cur   : h
		- right move cur  : l
		- move down cur   : j
		- move up cur     : k
		- del single word by cur :cw
		- serch word      : /
		- cancle          : u,ctrl+r
		- jump to line    : :100
		- jump to word start : w
		- jump to word end   : e
		- jump to brackets   : %
		- match word serch   : *
		- enter data at char back : a
		- enter data at char fornt : i
		- high liht word  : hls
		- cancle high light word : nohls
		- jump to char    : f + char
	-
- # understand
- ### 下载：
  understand下载：
  [Scitools Licensing | Download Understand](https://licensing.scitools.com/download/thanks/Windows-64bit.exe)
  破解工具下载：
  [Downloads | mh-nexus](https://mh-nexus.de/en/downloads.php?product=HxD20)
- ### 破解方法:
  :LOGBOOK:
  CLOCK: [2023-12-12 Tue 21:49:28]
  :END:
  复制一份 __understand.exe__ 在破解软件中打开，  按下 **Ctrl+F**   以文本方式 搜索
  > __areYouThere__
- 用下面的句子替代
- >__IamNotHere!__
- 回到顶部，以字节序列模式搜索
- >**45 33 FF 41 0F B6 C6 48 3B DF 44 0F 4E F8**
- 替换为
- >**41 BF 01 00 00 00 90 90 90 90 90 90 90 90**
- 最后替换安装路径下的 __understand.exe__
- ### 使用方法:
  [高效阅读嵌入式源码系列一：静态分析神器understand软件基本操作_eagle11235的博客-CSDN博客](https://blog.csdn.net/eagle11235/article/details/125210975)