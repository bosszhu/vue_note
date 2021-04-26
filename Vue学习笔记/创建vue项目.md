# 1. 创建vue项目
	1. 安装node.js环境
	2. 安装npm环境
	3. 安装vue/cli环境
2. 创建项目
	1. 可视化界面.
		1. vue ui->复制地址到浏览器打开
		2. 进行创建新项目.
	2. 命令行.
		vue create 项目名



打开项目文件夹理解其中一些文件的含义
1. package.json
	1. 包含的依赖以及版本
	2. vue的版本
	3. scripts 内含有serve,build,lint命令.
2. public文件夹
	含有index.html 包含<div id = "app"></div>
3. src文件夹
	


# Vue-router

路由管理工具
找到src文件夹下index.js文件.内部就是管理router工具.

1. 通过vue的google插件查看vue-router在网页中的路由
2. router创建新界面的步骤
	1. 创建.vue文件新界面
	2. app.vue内<div>标签内添加代码
			```
		    <router-link to="/info">Info</router-link>
		    ```
	3. 引入文件
		```
		import Home from '../views/Home.vue'
		```
	4. 配置路由文件路径
		```
		  {
			    path: '/info',
			    name: 'Info',
			    component: () => import('../views/Info.vue')
 		 }

		```



-----------
1. cmd + f ：搜索
2. cmd + opt + f： 替换
3. cmd + shift + f：在项目内搜索
4. opt+shift+b:插件快速打开浏览器