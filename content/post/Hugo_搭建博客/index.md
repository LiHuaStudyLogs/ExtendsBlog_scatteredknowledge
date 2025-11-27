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
* hugo 根目录：

	在下载的hugo_extents扩展包中，创建后需在其中加入hugo.exe执行文件，执行后续hugo命令操作  
    >创建命令行：
    >1. 基于下载的hugo扩展文件夹目录
    >2. hugo new site 根目录名称 
* themes 文件夹:

	主题文件夹，实现网页可视化的文件，其中的文件可以是自己创建或使用hugo官方的themes  
* content 文件夹：

	存放的[index.md](#index.md文件:)文章的存放地点
	> 创建命令行 :  
	> 1. 基于hugo根目录   
	> 2. hugo new post/文章名称/index.md
* public 文件夹 ：  

	生成在在根目录下，静态页面站目录，最终的网页html文件所在  
	> 创建命令行：  
	> 1. 基于hugo根目录   
	> 2. hugo - D
* hugo.yaml 配置文件：  
    配置hugo页面的属性设置，可以连接不同的themes，baseurl

 
## 要素二 ：过程  
1. hugo官方链接GitHub的分享文件夹下载，
2. 创建根目录、主题theme文件夹内容
3. 搭建网页：  
	> * 主目录下的hugo server -D命令行操作：  

	> 启动一个本地的临时服务器，具有自动生成public文件夹并上传到服务器（所以是实时的） —— 实现预览效果  
	> 由于是本地服务器，所以只能自己看
	***
	> * 在github网页上创建：  

	> github pages <sup>官方的静态托管服务</sup> 读取你指定的仓库中指定的public文件，他帮你托管成一个公开网站，可以给所有人看到 —— 实现public部署到 github pages   
	***
	> 部署的方式：  
		1. 手动部署，  
		内容刷新 ——> 生成public ——> 修改本地仓库的public ——> git commit -m"" + git push origin main ——> (实现推送新的内容) ——> 在 github pages 实现部署     
		2.	自动部署 <sup>github官方提供服务</sup>,   
		改造hugo文件夹：  
		根目录处操作：  
	    * 加入 .github文件夹/ workflows文件夹/ .yaml文件 ——> 拿到官方提供的代码 <sup>hugo官方有提供</sup> 配置 .yaml文件 ——> (替换里面的本地变量)  
		* 加入 .gitignore文件 ——> 写入 public<sup>必要忽略的文件夹</sup> 、resources、.hugo build.lock、hugo.exe ——> (这些对应的文件就不会上传到仓库)  
		*把 github pages 的source 配置成 github action  
		（此时）——> 执行git add .修改仓库内容(没有public文件夹) ——> 部署时会自动生成public结束后自动销毁



#### 插叙内容注解：


* #### index.md文件:  
    index文件就是先加载的文件 /  
    .md后缀就是文件支持[markdown语法](#markdown语法：) /


* #### markdown语法：
	markdown语法就是一种便捷式的文档书写语法。  

	> 空格*2 + 回车 --> 整体内框架换行  
	> 回车*2 --> 整体框架之间换行  
	> ** **加粗** **  
	> **斜体* *  
	> ***分割线  
	> #标题  
	> *无序列表 / 1.有序列表  
	> *[ ]框序列 / *[x] 勾选框列表  
	> ` ``` `语言  
		【代码块】  
	  `	``` `  
	> ``` `行内代码块`  ```  
	> ` > `引用  
	> ` [文本] `(链接) --> 跳转 / `[文本]`[变量] + 统一再[变量]: 链接 / `[文本]`(#标题)  
	> `![图片加载失败]`(地址)
	***
	> 表格  
	> | 1 | 2 | 3 | --> 表格头  
	| --- | --- | --- | --> 表格设置 ` :---: `表示数据居中   
	| a | b | c | --> 表体  
	> html 可用



   