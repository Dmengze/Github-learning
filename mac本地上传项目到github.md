### https方式（基础) 
#### 1:首先在github上创建好自己的账号和仓库. 
#### 2:记录仓库的https地址. 
#### 3:本地终端命令操作：  
- 1）cd: 切换到自己本地项目的更目录下. 
- 2）git init ; git初始化. 
- 3）git add . ; 把整个代码添加(整个项目). 
- 4）git commit -m "保存本地仓库说明" ; 提交至本地仓库. 
- 5）git remote add origin https://XXX.git ; 链接远程仓库. 
- 6）git pull origin master ; 从master分支上拉代码（如果是初次上传可以省略，但是做更改后一般都是有这步操作的）. 
- 7）git push origin master ; 提交本地仓库项目至远程仓库. 
- 8）输入git账户和密码. 
- 9）完成. 

## 完整版：
#### 一、增（上传新建项目）
  实际情况
  在本地开发了一个「angularJS-webApp」项目，需要将代码需要上传至GitHub。
  操作
- 1、在GitHub上新建一个项目，如：「angularJS-webApp」 项目
- 2、（先进入本地项目文件夹）通过命令 git init 把这个目录变成git可以管理的仓库
  > git init
- 3、把文件添加到版本库中，使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点“.”，意为添加文件夹下的所有文件
  > git add .
- 4、用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明
  > git commit -m '备注(自定义)'
- 5、关联到远程库
  > git remote add origin 你的远程库地址
  如：> git remote add origin https://github.com/bodanli159951/angularJS-webApp.git
- 6、获取远程库与本地同步合并（如果远程库「不为空」则必须做这一步，否则后面的提交会失败）
  > git pull --rebase origin master
- 7、把本地库的内容推送到远程，使用 git push命令，实际上是把当前分支master推送到远程。执行此命令后会要求输入用户名、密码，验证通过后即开始上传。
  > git push -u origin master
- 8、状态查询命令
  > git status
#### 二、增 上传新建分支
新建名为v4的分支：> git checkout -b v4  
  > git add
  > git commit -m"备注(自定义)"
  新建并提交到远程分支> git push --set-upstream origin v4
#### 三、删（删除分支）
如果要删除名为 v2的分支，必须切换到本地 git 的另一条分支上：�> git checkout master
删除本地v2分支操作：> git branch -d v2
- 1、删除远程分支：> git branch -r -d origin/v2
- 2、删除远程分支（准）：> git push origin -d v2
#### 四、改重命名分支
> git branch -m <old-branchname> <new-branch-name>
#### 五、查
  查询本地分支情况：> git branch
  查询本地和远程分支情况：> git branch -a


