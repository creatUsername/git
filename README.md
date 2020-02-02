# 什么是git?
  - 分布式 版本控制 工具

# 基本操作
  - git init 初始化
  - git status 检测当前文件夹文件管理状态
  - git add [filename] 管理文件
  - git commit -m [version/desc] 提交版本
  - git log 查看版本

# 三大区域
  - 1. 工作区
   - 受管理文件
   - 新文件 / 被修改文件 [红]
  * 操作
    - 提交文件到暂存区
    - git add [filename]

  - 2. 暂存区
   - 暂存区文件 [绿]
  * 操作
    - 提交到版本库
    - git commit -m [version/desc]

  - 3. 版本库
    * 操作
      - 版本回滚
      - git reset --hard [version] 回滚到指定版本