#### Q：vue生命周期（钩子函数）

**A：**beforeCreated、created(在created中可以首次拿到data中定义的数据)、beforeMount、mounted(此时dom树渲染结束，可以访问dom结构)、beforeUpdate、updated、beforeDestroy、destroyed

------

#### Q：computed中的getter和setter

**A：**

```js
computed: {
    fullName: {
        // getter
        get() => {
            return this.firstName + ' ' + this.lastName
        },
        // setter
        set(newValue) => {
			let names = newValue.split(' ')
            this.firstName = name[0]
            this.lastName = names[namge.length-1]
        }
    }
}
```

------

#### Q：watch监听对象（如何watch监听一个对象内部的变化）

**A：**

1.如果只监听obj内的某一个属性的变化，可以直接obj.key进行监听

```js
watch: {
    'obj.name'(newName,oldName) {
        this.getList()
    }
}
```

2、如果对整个obj深层监听

```js

```

