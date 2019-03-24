# 相关命令操作
## 基础操作
1. 初始化仓库
    - ` git init #用于初始化当前目录为一个git仓库 `
    - ` git init [dirname] #指定目录名为git仓库 `
2. 克隆一个仓库
    - ` git clone [repo] #克隆一个现有的仓库到当前项目，repo可以是本地仓库也可以是网上仓库的地址`
    - ` git clone [repo] [dirname] #克隆一个仓库到指定的dirname项目`
3. 将文件纳入版本控制
    - ` git add [filename] #添加filename到缓存`
    - ` git commit -m ['info'] #提交并保存info信息`
4. 查看状态
    - `git status -s #-s为查看简短的状态信息`
    - `git diff #查看缓存与当前文件的改动区别`
        - `git diff #查看尚未缓存的的改动`
        - `git diff --cached #查看已缓存的发动`
        - `git diff HEAD #查看已缓存与未缓存的所有改动`
        - `git diff --stat #显示摘要信息`
5. 取消已缓存命令
    - `git reset HEAD #用于取消已经缓存的文件（使用git add提交过的）`

6. 删除文件
    - `git rm [filename]`
        - -f参数用于强制删除已经提交到暂存区的文件
    - **使用该命令删除文件时，需要提交才会真的删除仓库内的文件**
7. 移动或重命名
    - `git mv [filename] #文件可以是普通文件、目录、软连接`

##分支管理
1. 创建分支
    `git branch [branchname]`
    - -b参数为创建分支并立刻切换到分支
2. 切换分支 
    `git checkout [branchname]`
3. 合并分支 
    `git merge`
4. 查看所有分支
    `git branch`
##查看提交历史
1. 查看提交历史
    - `git log`
        - --oneline参数可以查看历史记录的简洁版
        - --graph 参数可以查看拓扑图
        - --reverse 参数为逆向显示所有日志 
        - --author=[username]用于显示指定用户提交的信息
## 标签
*标签的一个作用是版本的显示，如当仓库内的项目完成到了一定程度，就可以使用git的标签功能，为项目打上一个版本信息*
1. 添加标签
    - `git tag -a V1.0`
        - -a 参数可以为标签添加额外的备注信息.
2. 追加标签
    - `git tag -a [V0.9] [id号]`
3. 查看所有标签
    - `git tag`
4. 指定标签信息
    - `git tag -a [tagname] -m [info]`

##远程仓库
1. 添加远程库
    - `git remote add [shortname] [url]`
    - 生成SSH-Key
        `ssh-keygen -t rsa -C "838010074@qq.com"`
            - 邮箱地址为github注册的地址
    - 打开用户家目录的.ssh文件，复制id_isa.pub里面的key到github上进行设置 
    

    
    



