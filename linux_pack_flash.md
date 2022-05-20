## Sd_Card_Tool  ( fdisk )
1. sudo fdisk -l
```
列出 所有 磁盘设备
sdcasrd_type : mmcblk    sdb      
```
2.  sudo fdisk /dev/mmcblk0
```
    选中要操作的磁盘设备
```
3. p
```
    打印分区表
```
4. d 1
```
    删除分区1
```
5.  n
```
    新建分区
```
6.  w
```
    分区表写入磁盘
```
7.  ls /dev/ | grep mmcblk0
```
    查看 mmcblk0 磁盘分区
```
