# Vue模板语法
1. 认识Vue结构
	1. templete
	2. script
	3. style
2. 特殊指令以及含义,事件绑定.
el,data,methods
	1. v-html:div代码块
	2. v-bind:(元素绑定属性)--->缩写:
	3. v-on:(绑定事项)-->缩写@

```
<script src="https://cdn.bootcdn.net/ajax/libs/vue/2.6.9/vue.min.js"></script>


<style>
   .bg {
       color: red;
   }
</style>


<div class="bg">
    <div>
        {{msg}}
        {{count}}
    </div>
    <div v-html="template">
    </div>
    <a v-bind:href="url1">百度</a>
    <a :href="url1">百度简写</a>
    <button type="button" v-on:click = "submit()">加数字</button>
    <button type="button" @click = "submit1()">减数字</button>
</div>

<script>
    new Vue({
        el: '.bg',
        data: {
            msg: 'hello vue!',
            count : 1,
            template:'<div>hello template</div>',
            url1:'http://www.baidu.com'
        },
        methods: {
            submit:function() {
                this.count++;
            },
            submit1: function() {
                this.count--;
            }
        }
    })
</script>

```


##### 注意:
调试窗口快捷键:cmd+opt+i