 安装git git apt-get install git
 安装完成后，进一步设置：
 git config --global user.name "SweeneyXue"
 git config --global user email "sweeneyxue@gmail.com"
 设置完成后，使用git.（创建一个版本库文件）
 mkdir learn-document 创建一个文件夹
 cd learn-document 进入这个文件夹
 git init  初始化该文件夹
 vim -o2 README.md readme.txt   创建自己的文本文件
 文件创建完毕,
 git status 查看版本控制情况
 git add README.md readme.txt 提交到暂存区
 git commit -m "creates documents" 提交到当前分支下

 git log 查看提交状况
 git reset -- hard HEAD^ 回退到上一版本
 git reset -- hard id号  回退到ID号所在版本

 git reflog 查看历史提交版本号
 git checkout -- 文件名  撤销工作区的修改
 git reset HEAD 文件名 撤销暂存取的修改

 提交分支后，工作区删除一个文件
 若版本分支也删，命令是：
 rm test.txt
 git rm test.txt
 git commit -m "remove test.txt"
 提交分支后，工作区删除一个文件
 想要恢复，命令是
 rm test.txt
 git checkout -- test.txt
 
 文件修改完毕，github上创建了项目，提交远程库的命令
 git remote add origin git@github.com:SweeneyXue/learn-document.git
 
git push -u origin master

完成备份

注意：有时github上已经有文件，版本库不对应，可以强制上传，命令是：
git push -u origin maste -f (有重要文件在，不建议这么做)


