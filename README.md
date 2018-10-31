1. 安装git git apt-get install git
2. 安装完成后，进一步设置：
3. git config --global user.name "SweeneyXue"
4. git config --global user email "sweeneyxue@gmail.com"
5. 设置完成后，使用git.（创建一个版本库文件）
6. mkdir learn-document 创建一个文件夹
7. cd learn-document 进入这个文件夹
8. git init  初始化该文件夹
9. vim -o2 README.md readme.txt   创建自己的文本文件
10. 文件创建完毕,
11. git status 查看版本控制情况
12. git add README.md readme.txt 提交到暂存区
13. git commit -m "creates documents" 提交到当前分支下

14. git log 查看提交状况
15. git reset -- hard HEAD^ 回退到上一版本
16. git reset -- hard id号  回退到ID号所在版本

17. git reflog 查看历史提交版本号
18. git checkout -- 文件名  撤销工作区的修改
19. git reset HEAD 文件名 撤销暂存取的修改

20. 提交分支后，工作区删除一个文件
 若版本分支也删，命令是：
21. rm test.txt
22. git rm test.txt
23. git commit -m "remove test.txt"
24. 提交分支后，工作区删除一个文件
 想要恢复，命令是
25. rm test.txt
26. git checkout -- test.txt
 
27. 文件修改完毕，github上创建了项目，提交远程库的命令
28. git remote add origin git@github.com:SweeneyXue/learn-document.git
 
29. git push -u origin master

完成备份

注意：有时github上已经有文件，版本库不对应，可以强制上传，命令是：
git push -u origin maste -f (有重要文件在，不建议这么做)

30. 若想下载github上的文件，比如一份markdown文件，命令是：
git clone git@github.com:xirong/my-markdown.git

完成下载
