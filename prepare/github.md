# 代码仓库

Github 是多人协作开发工具，支持多人同时开发同一个项目，为满足多人大型项目的不断迭代，提供了各种代码管理方式。

对于初学者而言，只需要掌握 Github 最基本的操作即可，简单说就是在服务器端为项目创建仓库，不断提交本地编写的代码。

主要有
```
git clone：克隆已有仓库
git add：添加修改内容
git commit：添加修改备注
git push：提交代码到服务器
git pull：从服务器拉取代码，多人协作或换电脑时需要
```

## 官方相关文档：
1. 注册账号 https://docs.github.com/cn/get-started/signing-up-for-github/signing-up-for-a-new-github-account
2. 安装配置桌面版软件 https://docs.github.com/cn/desktop/installing-and-configuring-github-desktop
3. 官方快速入门 https://docs.github.com/cn/get-started/quickstart/hello-world
4. 添加和克隆仓库 https://docs.github.com/cn/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/adding-a-repository-from-your-local-computer-to-github-desktop
5. 修改提交 https://docs.github.com/cn/desktop/contributing-and-collaborating-using-github-desktop/managing-commits/amending-a-commit
6. 词汇表 https://docs.github.com/cn/get-started/quickstart/github-glossary

## 提交方法

项目一般都是多个文件，一定出于某个目才会修改代码，而为了达成某个目的，经常需要修改多个文件，甚至还会增删文件、重命名文件等。因此推荐以事件为单位组织提交，事件 A 修改了文件 1，事件 B 修改了文件 1、2、3，正确的操作方式为：
1. 先修改文件 1 完成事件 A，添加修改，在说明中填写修改原因，即事件 A，如果事件 A 有说明链接，一并写入
2. 继续修改文件 1、2、3，添加修改，在说明中写入事件 B 并附加链接

这样做的好处是避免文件变动带来的影响，回溯记录时，可以按照具体的活动顺序管理，更符合事情的实际情况。

## gitignore 的配置使用

本地开发时，项目文件夹中会有很多真正代码之外的文件，可能有编辑工具生成的，也可能有开发临时需要的一些文件，这些文件都不会作为最终文件发布，也无须进行备份，因此需要在提交时进行过滤。
gitignore 可以方便的过滤不需要备份的文件，具体做法是在项目根目录创建一个名字为 `.gitignore` 文件，文件名看着有点怪，但一定不能做任何修改。
创建后用代码编辑工具打开文件填写内容，示例如下，支持 `*` 通配符，`# ` 为注释语法：

```
node_modules
dist
dist-ssr
*.local

# Editor directories and files
.vscode/*
!.vscode/extensions.json
.idea
.DS_Store
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?
```


## 注意事项：
1. 和分支、tag 相关的部分可跳过，先尽快掌握代码提交保存
2. 一个项目一个仓库，仓库之前保持隔离，不可交叉
3. 先在服务器端创建好仓库，再同步到本地添加代码
4. 必须掌握的操作，创建单独项目训练，切忌在正式的项目中进行未知操作


## 扩展阅读：

1. Git提交日志规范 https://cloud.tencent.com/developer/article/1404933
2. Commit message 和 Change log 编写指南
 https://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html
3. 简明教程 https://www.runoob.com/w3cnote/git-guide.html
4. Github Docs https://docs.github.com/cn/get-started/getting-started-with-git/ignoring-files