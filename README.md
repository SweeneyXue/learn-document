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
> 创建分支，改变分支，删除分支
31. git branch -b dev 创建分支dev，并切换分支
> 上面的命令相当与下面两条命令
32. git branch dev 创建dev分支
33. git checkout dev 切换到dev分支
34. 查看分支的命令是：git branch
35.分支完成工作，切换回master分支的命令是：git checkout master
36. 合并分支的命令是：git merge dev
37. 删除分支的命令是：git branch -d dev
> 完成
> 分支管理
> cheshi
> Bug 分支管理
38. 保存当前工作的现场的命令是:git stash
> 保存现场，推出当前分支，修复bug后，回到工作分支的方法有两种首先使用命令git stash list 查看保存的工作有那些，找到现场进行恢复，第一种方法是：git stash apply 进行恢复，stash内容不删除，需用git stash drop进行删除。第二种方法是使用git stsh pop ,恢复的同时删除stash内容。（一般用第二种方法）
> 完成



> 创建了一个新分支开发新功能，创建成功，开发完成，切换回工作分支后，还未合并，需要删除，命令是:git branch -D fenzhiming

>




39. 通常master分支仅仅用来发布新版本的，（平时不在上面干活）
40. dev分支是项目组各个成员干活的地方，（自己完成开发合并到master分支上）
41. Bug分支通常在本地，自己的目录中随时修复
42. 新功能分支



>
>
>
43. 多人协作开发

你的小伙伴从远程下载该项目的命令 git clone git@github.com:SweeneyXue/learn-document.git ~/learn/
  
- 利用git checkout -b dev origin/dev 创建dev分支，并切换到dev目录下，并且连接到远程库的dev分支下

44. 当其他人已经改变了dev分支的内容，并且推送到了远程，我再推送的时候，会发生什么呢?
45. 其他人推送，自己再推送会发生冲突，利用git pull从最新的origin/dev上抓下来，再在本地合并，解决冲突，
46. 当git pull 失败，提示，没有指定本地dev分支与远程origin/dev分支的链接，根据提示设置dev和origin/dev的链接，命令是：git branch --set-upstream-to=origin/dev dev
47. 然后在git pull成功，合并时有冲突，自己动手解决，然后在提交。
> 完成
>
>
>
>

