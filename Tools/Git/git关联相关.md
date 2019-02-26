
- [git 本地分支与远程分支关联的一种方法](https://www.cnblogs.com/a-flydog/p/5520999.html)
- [git stash相关](https://blog.csdn.net/wh_19910525/article/details/7784901)

情况1:
  在本地电脑上有一个项目文件project,想将其放到github上托管
操作:
  1.在github上创建一个仓库repository,比如名叫test_project,并复制其ssh地址
  2.进入本地项目文件project,执行git init将本地目录变为工作区
  3.执行git remote add origin git@github.com:XXX/test_project.git,将本地与远程仓库关联起来
  4.一定要执行一次git pull origin master,将远程的东西拉取下来,因为有可能在创建repository时会选择创建一些文件
  5.执行git add将项目中的其它文件提交到暂存区,
  6.之后git push --set-upstream origin master , 再git push 推送到远程仓库
  
情况2:
  在本地电脑上如何从远程拉取一个非master分支,比如dev分支,在本地创建dev分支或改了名的分支与dev分支对应
操作:
  1.在本地上git branch -a查看远程所有分支
  2.选择你要拉取的分支,比如remotes/origin/dev分支,执行git checkout -b dev origin/dev
  3.你已经切换到本地dev分支并与远程dev分支关联了起来
  4.用git branch -vv 查看当前本地的dev分支关联的是不是origin/dev

情况3:
  如果用git checkout -b dev创建了本地dev分支,但并未和远程的关联(远程已经存在origin/dev分支),想把两者关联起来,怎么办?
操作:
  1.切换到你已经创建但还未关联的dev本地分支,git branch dev
  2.在本地上git branch -a查看远程所有分支
  3.选择你要关联的分支,比如remotes/origin/dev分支,执行git branch --set-upstream-to=origin/dev
  
- 情况4:
  - 如果用git checkout -b dev创建了本地dev分支,想和远程分支关联(远程还未创建dev分支),想把本地分支推送到远程,怎么办?
- 操作:
  1. git checkout -b dev  (一定要切换到dev分支)
  2. git push origin dev:dev  (在远程推送一个dev分支,同时将远程dev分支与当前dev分支关联)
  或者
  1. git checkout -b dev  (一定要切换到dev分支)
  2. git push origin dev  (在远程推送一个dev分支)
  3. git branch --set-upstream-to=origin/dev  (将远程dev分支与当前分支关联起来)
  

  
  
