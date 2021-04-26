# 条件渲染
v-if
v-else if
v-else
v-show
```
    <div id="app">
        <div v-if="count > 0">
            count > 0,count的值是{{count}}
        </div>
        <div v-else if="count = 0">
            count = 0,count的值是{{count}}
        </div>
        <div v-else="count < 0">
            count < 0,count的值是{{count}}
        </div>
    </div>
```
# 列表渲染
v-for
```
	//显示
	<div v-for="item in list">
	    {{item.name}}
	</div>

	//数据源
    <script>
    var app = new Vue({
        el: '#app',
        data: {
            count:0,
            // list:[1,2,3,4]
            list:[{
                name:'jack',
                age:13
            },{
                name:'rose',
                age:13
            },{
                name:'bob',
                age:13
            }]
        }
    })
</script>
```
# style和class的绑定

v-bind



