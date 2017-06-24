 gulp的使用
---------------------------------------------------------------
一、简介
-----------------
	gulp是前端开发过程中对代码进行构建的工具，是自动化项目的构建利器；它是基于Node.js的自动任务运行器。
	本示例就对它的安装和使用和大家一起学习。

二、安装
-----------------
	1.因为gulp是基于node.js的，所以在安装gulp之前，先安装nodejs；打开node的官网，下载适合自己机型的文件，
	然后像安装QQ一样，N个下一步（路径建议放在C盘）。通过window+r 输入cmd回车，然后输入node-v查看node的版本信息，
	如果出现版本信息，说明安装成功

三、npm的介绍
-----------------
	1.npm是nodejs的包管理管理器，用于管理node中的插件

	2.使用npm来安装插件：命令符→ npm install <name> -g --save-dev
		a.<name>:是node插件名称。如：npm install gulp-less --save-dev
		b.-g：表示全局安装
		c.--save:表示将配置信息保存至package.json中
		d.-dev:表示保存至package.json的devDependencies节点

	3.npm插件的卸载：npm uninstall <name> [-g] [--save-dev]

	4.使用npm更新插件：npm update <name> [-g] [--save-dev]

四、安装cnpm
-----------------
	1.ps：因为npm安装插件是从国外服务器下载，受网络影响大，可能出现异常；

	2.在实际工作中，我们会经常使用淘宝镜像来用npm来代替cnpm

	3.安装：命令提示符执行npm install cnpm -g --registry=https://registry.npm.taobao.org；
	注意：安装完后最好查看其版本号cnpm -v；cnpm跟npm用法完全一致，只是在执行命令时将npm改为cnpm

五、gulp的安装
--------------------
	1.全局安装：全局安装gulp目的是为了通过它执行gulp任务

	2.安装命令：cnpm install gulp -g

	3.局部安装：找到D盘，新建一个gulp文件夹，然后通过dos命令，找到当前文件，输入命令：cnpm init  
	会自动创建一个package.json文件，然后显示如图下：
	![image text](https://github.com/fupan1018/gulp/blob/master/src/img/gulp05.png)

	4.为了能正常使用，在本地安装gulp：cnpm install gulp --save-dev；

	5.安装插件；如：cnpm install gulp-less --save-dev(经过后面的配置可以对less文件进行编译)

六、新建gulpfile.js文件
----------------------------
	1.说明：gulpfile.js是gulp项目的配置文件，是位于项目根目录的普通js文件

	2.新建一个生产文件和一个输出文件(文件结构如下图)
	http://github.com/fupan1018/gulp/src/img/gulp01.png

	3.安装的所有插件，都会在这儿进行配置

	4.部分配置如下图(更加详细的见文件gulpfile.js)

	引入插件
	http://github.com/fupan1018/gulp/src/img/gulp02.png

	配置插件
	http://github.com/fupan1018/gulp/src/img/gulp03.png

	运行gulp
	http://github.com/fupan1018/gulp/src/img/gulp04.png

七、运行gulp
-----------------------------
	1.命令提示符执行gulp 任务名称

	2.或者运行多个任务，将任务配置到default中，直接运行gulp就会调用default中的任务
