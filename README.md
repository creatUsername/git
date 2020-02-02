# 什么是git?
  - 分布式 版本控制 工具

# 基本操作
  - git init 初始化
  - git status 检测当前文件夹文件管理状态
  - git add [filename] 管理文件
  - git commit -m [version/desc] 提交版本
  - git log 查看版本

# 三大区域
  - 1. 工作区 [working-directory]
    - 受管理文件
    - 新文件 / 变动文件 [红]
    * 操作
      - 提交文件到暂存区
      - git add [filename]

      - 还原变动文件
      - git checkout [filename]

  - 2. 暂存区 [staging-area]
    - 暂存区文件 [绿]
    * 操作
      - 提交到版本库
      - git commit -m [version/desc]

      - 回溯到 工作区(新/变动文件)
      - git reset HEAD

  - 3. 版本库 [repository]
    * 操作
      - 查看版本
        - git log(版本日志) * 看不到回退版本号之后的版本记录
        - git reflog(操作日志) * 版本回退后,仍然可以看到所有的版本记录

      - 版本还原至 工作区(受管理文件)
      - git reset --hard [version]

      - 版本还原至 工作区(新/变动文件)
      - git reset --mix [version]

      - 版本还原至 暂存区
      - git reset --soft [version]

# 分支 [branch]
  - [master] 主支
  - [branch-name] 分支

  * 操作
    - 查看分支
    - git branch
    - 创建分支
    - git branch [branch-name]
    - 进入分支
    - git checkout [branch-name]
    - 创建并进入分支
    - git checkout -b [branch-name]
    - 删除分支
    - git branch -d [branch-name]
    - 合并分支
    - git merge [branch-name] * 先切换到要合并的分支

  - 简单工作流
    - master [线上分支]
    - dev [开发分支]
    - bug [BUG分支]

# github
  - 线上代码托管仓库
  
  * 操作
    - 链接远程仓库
    - git remote add origin [url] 远程仓库地址
    - 代码推送到分支(-u 默认参数以后可以使用git push 代替 git push origin master)
    - git push -u origin [branch]
    - 克隆远程仓库代码(默认实现远程仓库链接)
    - git clone [url]
    - 拉取远程仓库代码
    - git pull origin [branch]