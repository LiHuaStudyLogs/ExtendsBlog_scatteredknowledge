+++
date = '2025-11-26T01:32:42+08:00'
draft = false
title = 'Hugo_搭建博客'
+++

**原理** ：

1.Blog : 就是一个网页
2.hugo : 是一个提供的文件夹，用于高效搭建页面的前端开发工具，  
官方下载的其中包含许多的配置文件，用于 ***画页面***

# **创建要素**
## 要素一 ：hugo配置文件的重要文件  
* hugo根目录：

	在下载的hugo_extents扩展包中，创建后需在其中加入hugo.exe执行文件，执行后续hugo命令操作  
    >创建命令行：
    >1. 基于下载的hugo扩展文件夹目录
    >2. hugo new site 根目录名称 
* themes文件夹:

	主题文件夹，实现网页可视化的文件，其中的文件可以是自己创建或使用hugo官方的themes  
* content文件夹：

	存放的[index.md](#index.md文件:)文章的存放地点
	> 创建命令行 :  
	> 1. 基于hugo根目录   
	> 2. hugo new post/文章名称/index.md
* public文件夹 ：  

	生成在在根目录下，静态页面站目录，最终的网页html文件所在  
	> 创建命令行：  
	> 1. 基于hugo根目录   
	> 2. hugo - D
* hugo.yaml配置文件：  
    配置hugo页面的属性设置

 
## 要素二 ： 

#### 插叙内容注解：

* #### index.md文件:  
    index文件就是先加载的文件，/  
    .md后缀就是文件支持[markdown语法](#markdown语法：)/
* #### markdown语法：
        
