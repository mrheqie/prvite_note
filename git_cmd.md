# use_cmd
## git add f_n
    添加fn文件到暂存区
## git commit -m 'description'
    将暂存区的内容提交到版本库中 单引号内为这次提交的描述
## git status
    查看当前是否有内容未提交
## git diff f_n
    比较当前f_n文件和版本库中的f_n文件有和差异
## git log
    查看提交日志
    git log --pretty=oneline    简洁版
    git reflog  代版本号的
## git reset --hard 版本号
    恢复到版本号所指定的版本
    git reset --hard HEAD^  回滚到上个版本
## git checkout -- f_n
    撤销本次对 f_n 文件的操作
## git init  --bare f_n.git
  创建一个空的仓库
## sudo  chown -R git:git f_n.git/
    把Git仓库的所有者修改为git
## git remote add f_n ssh://255.255.255.255/hone/././.
    添加远端仓库
## git remote set-url  f_n ssh://255.255.255.255./home/./.
    修改远端仓库地址
## git push f_n master
    推送到远端仓库
## git clone ssh:git@255.255.25.255:/home/./.
    克隆远端仓库的内容    
    