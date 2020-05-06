---
title: depoly by git
date: 2020-04-30 16:45:51
tags:
  - [git]
  - [hexo]
category:
  - [前端]
---

* 玩了一会  
* 发现hexo其实可以自动部署
* 可以选择用git
* 配置文件加一点配置就好

  ~~~
  deploy:

    type: git
    repo: <repository url> 
    branch: [branch]
    message: [message]

  ~~~

* 再用下面的命令

  ~~~
  hexo generate --deploy
  ~~~
---

> 这样就可以在生成静态文件的时候自动发布了
