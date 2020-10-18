# CMD_BASE
<br>

* **rm -rf  文件**  
    递归删除

# NFS  

*   **sudo apt install nfs-kernel-server**  
    安装NFS服务
*   **id**  
    查看用户id
* **sudo vim /etc/exports**  
    打开NFS配置文件
*   **mkdir  /home/embedfire/workdir**  
    创建共享目录
*   **/home/embedfire/workdir 192.168.0.0/24(rw,sync,all_squash,anonuid=998,anongid=998,no_
subtree_check)**
    NFS配置语句，将此句写入exports文件内
*   **sudo exportfs -arv**
    更新exports配置
*   **showmount -e** 
    查看NFS服务器的加载情况  
<br>
<br>  
*   **sudo apt install nfs-common -y**  
    安装NFS客户端
*   **showmount -e 192.168.0.219  **  
    查看远端NFS共享目录  
*   **sudo mount -t nfs 192.168.0.219:/home/embedfire/workdir /mnt**  
        挂载NFS远端目录到本地 
*   **sudo umount /mnt**  
        取消挂载

* **ssh connect**
    ssh hebing@255.255.255.255  

