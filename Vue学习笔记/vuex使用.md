# vuex使用
怎么将一个页面的事件传递到另一个页面?

1. 事件页面内
	1. 一个页面创建事件,vue内创建事件实现.
	2. 该页面<scripts></scripts>内引入store文件,并且进入store属性.
	3. 在事件实现store.commit('function')



2. Vuex内
	1. state内注册属性
	2. mutations调用方法改变值得变化



3. 监听页面内
	1. 引入store
	2. 通过store.state.count(count代表Vuex内注册的属性).拿到属性值.

---
相关代码:
事件页面内:
```
		//1. div创建事件
	    <div class="Info">
        <h1>this is a Info Page</h1>
        <button type="button" @click="add()">添加</button>

        //2. 引入store,methods内的方法实现内,通过store.commit提交事件管理者vuex内的事件
        import store from '@/store'
    	export default {
        	store,
        	methods: {
           	 add() {
                console.log('add a Info event')
                store.commit('increasa')
          	 }
      	 	},
    	}
   		 </div>
```
Vuex内:

```
	//组件状态,注册属性
  	state: {
    	count : 0
  	},
  	  //唯一改变vuex的状态集,此处实现state内注册属性的状态改变
  	mutations: {
    	increasa() {
     		 this.state.count++
   		 }
  	},

```

监听页面内:
```
	//引入store,data内通过store.state获取属性改变后的值
	import store from '@/store'
  	export default {
    name: 'about',
    data() {
      return {
        msg: store.state.count
      }
    },
  }

```


