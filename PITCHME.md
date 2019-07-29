# Git内部培训课件
---
## Git简介
### 什么是版本控制

版本控制系统（Version Control System，简称VCS）是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统。

---
按类型可以分为：
- 本地版本控制系统
![v1](https://upload-images.jianshu.io/upload_images/3789468-aa800a1a5658a7d5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/400/format/webp)

例如RCS（至少我是从来没有用过）
本地版本控制系统解决了版本的管理问题，再也不用时不时的把工程目录，通过手工拷贝的方式来存档了。但本地版本控制系统的缺点是，无法解决多人协作的问题。

---
- 集中化的版本控制系统
![v2](https://upload-images.jianshu.io/upload_images/3789468-e81709571bd11a60.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/500/format/webp)

例如CVS，SVN等（公司中SVN应该用的比较多）
有一个集中管理的服务器，所有开发人员通过客户端连到这台服务器，取出最新的 文件 或者提交更新。管理员可以掌控每个开发者的权限。
集中化的VCS不但解决了版本控制问题，还可以多人协作。但缺点也是有的，就是太依赖于远程服务器，CVS服务器宕机后，会影响所有人的工作。版本记录只保存在一台服务器上，会有数据丢失风险。

---
- 分布式版本控制系统
![v3](https://upload-images.jianshu.io/upload_images/3789468-2e759b90b7f8216a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/500/format/webp)

例如Git
客户端并不只提取最新版本的文件，而是把 代码仓库 完整地镜像下来。每一次的提取操作，实际上都是一次对 代码仓库 的完整备份。
所以并没有"中心服务器"的概念，所谓的"Git服务器"，也同每个人的电脑一样，只是为了多人协作时，方便大家交换数据而已