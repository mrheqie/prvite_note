- [**use\_cmd\_base**](#use_cmd_base)
- [**use\_cmd\_remote**](#use_cmd_remote)
- [**use\_cmd\_branch**](#use_cmd_branch)
- [**file\_parse**](#file_parse)


# **use_cmd_base**
 <br>

*  **git init**   
    新建一个仓库  
    --bare 新建裸仓库 没有文件目录  
    --shared 新建的仓库可写

*  **git add f_n**  
    添加fn文件到暂存区
* **git commit -m 'description'**  
    将暂存区的内容提交到版本库中 , 单引号内为这次提交的描述       
    加入-a 选项可以直接提交已经跟踪过的文件  不用使用 git add  
*   **git status**    
    查看当前是否有内容未提交
*  **git diff f_n**  
    比较当前f_n文件和版本库中的f_n文件有和差异
*  **git log** 
    查看提交日志  
    git log --pretty=oneline    简洁版  
    git reflog  代版本号的  
*  **git reset --hard 版本号**  
    恢复到版本号所指定的版本  
    git reset --hard HEAD^  回滚到上个版本  
*  **git checkout -- f_n**  
    撤销本次对 f_n 文件的操作
*  **git init  --bare f_n.git**  
    创建一个空的仓库
*  **sudo  chown -R git:git f_n.git/**  
    把Git仓库的所有者修改为git
* **git log --graph --oneline**
    打印log
*  **git rm**  
    从仓库中移除文件但本地保留  
    --cached f_n  从仓库中移除但本地保留  
    \\*    通配符
*  **git mv f_n1 f_n2**  
    重命名文件

*  **git config --global user.name "hebing-y9000x"**  
    配置用户名
* **git config --global user.email "434631138@qq.com"**  
    配置邮箱

* **git status --ignore-submodules=dirty**  
    忽略脏的子模块

*   **sudo git branch -D master**
    删除主分支

 <br>

# **use_cmd_remote**
 <br>

*  **sudo  chown -R git:git f_n.git**  
    远程仓库创建后需要把所有者改为git  

*  **git remote**  
    查看远程仓库  
    -v 查看远程仓库的地址  
*  **git remote show 远程仓库名**  
    查看远程仓库的详细信息  
*  **git remote add f_n ssh://git@255.255.255.255/hone/././.**  
    添加远端仓库
*  **git remote set-url  f_n ssh://git@255.255.255.255./home/./**  
    修改远端仓库地址
* **git pull**    
    从远端仓库拉取最新
* **git push 远程仓库名 master**  
    推送到远端仓库  
* **git clone git@192.168.31.189:/home/hebing/git_repos/note_repo/note.git**
    克隆远端仓库的内容     
*  **git fetch 仓库名**  
    下载本地与远程不同的部分 ，但并不合并  
* 切换默认远端仓库地址
```
git config branch.master.remote 远端地址 远端别明
git config branch.master.merge refs/heads/master
```
 <br>

# **use_cmd_branch**
 <br>

*  **git branch**  
    查看当前所有分支

*  **git branch 分支名**  
    新建分支  
*  **git checkout 分支名**  
    切换到分支  
*  **git checkout -b 分支名**  
    创建并切换到分支  
*  **git  merge  分支名**  
    将指定分支与当前分支合并  
*  **git branch -d f分支名**  
    删除分支
 <br>

# **file_parse**
 <br>

*  **.gitignore**  
    内部为仓库要忽略的文件  
    example:   
    *.[oa ] 忽略所有以.o和.a结尾的文件  
     *~ 忽略以~为结尾的文件  
    builld/  忽律build目录下的文件
