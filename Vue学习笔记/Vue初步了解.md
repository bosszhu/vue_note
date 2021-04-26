# Vue使用
1. 安装vscode
2. 命令行安装node.js
3. 创建html文件
	1. cmd+s,保存格式为html
	2. 创建代码块,快捷键!加tab
4. 使用CDN直接引用Vue.
	1. js中创建vue对象.
		1. el绑定相应class或id.
		2. data绑定数据
	2. body内获取data内数据内容.就可以玩完成动态变化

### 简单代码应用
```
//cdn引入vue框架
<script src="https://cdn.bootcdn.net/ajax/libs/vue/2.6.9/vue.min.js"></script>

//style代码:
    <style>
       .bg {
           color: red;
       }
    </style>


//body代码:
    <div class="bg">
        hello world!
        {{msg}}
    </div>


//script代码:
    new Vue({
		el: '.bg',
        data: {
            msg: 'hello vue!'
        }
    })
```


##### 注意点:
1. 语法格式{{}}以及Vue创建和内部元素构成new Vue({})
2. 页面刷新需要cmd+s先保存代码,刷新快捷键cmd+shift+R


