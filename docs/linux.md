# CMD_BASE
<br>

* **rm -rf  文件**  
    递归删除
* **authority**
```
    linux uses 5 numbers to indicate variousl permissions 
     first num : set user id
     second num : set group id
     third num : indicate user permissons
     fourth num : indicate group permissons
    fifth num : indicate others permmissons

    num first bit : execution authority
    num second bit : write authority
    num third bit : read authority

    example :
     00777 means that  all users are authorized to write,read and execute permissions
      

```
# NFS

*   **sudo apt install nfs-kernel-server**  
    安装NFS服务
*   **id**  
    查看用户id
* **sudo vim /etc/exports**  
    打开NFS配置文件
*   **mkdir  /home/hebing/nfs**  
    创建共享目录
*   **/home/hebing/nfs 192.168.31.*(rw,sync,all_squash,anonuid=998,anongid=998,no_
subtree_check)**
    NFS配置语句，将此句写入exports文件内
*   **sudo exportfs -arv**
    更新exports配置
*   **showmount -e** 
    查看NFS服务器的加载情况  
* **sudo service nfs-kernel-server restart**
    重启NFS服务
<br>  
<br>    
*  **sudo apt install nfs-common -y**  
    安装NFS客户端
*   **showmount -e 192.168.0.219  **  
    查看远端NFS共享目录  
*   **sudo mount -t nfs 192.168.31。189:/home/hebing /nfs   /home/hebing/c_nfs  
        挂载NFS远端目录到本地 
*   **sudo umount /home/hebing/c_nfs  
        取消挂载
# SSH

* **ssh connect**  
    ssh hebing@255.255.255.255  

# MODULE

* **install module** 
```
    insmod   ./hello.ko
```
* **uninstall module**
```
    rmmod   hello
```
* **view all module**
```
    lsmod
```
* **install module and its dependencises**
```
    modprobe
```  
* **unstall modeule and its dependencises**
```
    modprobe -r < filename>
```
* **get info about  a module**
```
    modinfo < modname>
```
