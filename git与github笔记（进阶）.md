### 同步到远程仓库
    查看远程仓库名：
        git remote  (默认origin)

    查看上传地址和下载地址是否为一个地址
        git remote -v
    
    创建远程仓库
        git remote add 名字 github的地址

    上传远程仓库
        git push origin(默认) master

    
# 协作
###     需要创建项目者给协作者权限
        进入项目 -> settings -> 
        最左边 Collaborators -> 添加协作者名字

###     等待协作者确定

    协作者：
        1.确定协作
        2.clone项目
        3.参与项目开发
        4.提交上传

###     有可能会遇到冲突:
        git pull (直接把远程的代码覆盖到本地)（不太推荐）

        git fetch (把远程仓库的代码拉取下来不覆盖)

###        查看哪里有冲突
            git diff master origin/master

###  合并冲突
            git merge origin/master  (你会发现master变成了matser|MERGEING)

            人为判断冲突，把冲突内容删除

            删除完成之后（代码被修改了，需要重新提交）

            保存到版本区之后，继续push （matser|MERGEING就变成了master）

### 没权限协作：
    1. 找到想参与的项目fork
    2. 把项目克隆到本地 -> 修改 -> 提交
    3. 点击 Pull requests
    4. 点击 new pull request
    5. 点击 Create pull request
    6. 对话点击Create pull request
    7. 等待
    
### 收到修改消息
    1. 点击修改的消息
    2. 点击files changed（查看修改内容）
    3. merge pull request(可以回复别人)


## 分支：
### 新建分支：
   	git branch 分支名
   
### 查看分支:
   	git branch
   	
### 切换分支:
   	git checkout 分支名
   
###  快速创建 + 切换
   	git checkout -b 分支名
   	
### 合并分支:
   	git merge 分支名
   	
### 可能会出现冲突:
   		人为修改文件 -> 提交
   	
### 删除已经合并的分支:
   	git branch -d 分支名
   
###  删除未合并的分支:
   	git branch -D 分支名
   	
###    查看已经合并的分支:
   	git branch --merged
   	
###    查看未合并的分支:
   	git branch --no-merged
