#HTML Forms 表单

### form 元素

```
<form>
...
</form>
```

一般用于用户输入的区块

### input 元素

*	`<input type="text">` 定义一个文本输入框
*  `<input type="radio">` 定义一个radio按钮（多选一）
*  `<inout type="submit">` 定义一个提交按钮

### `action` 属性

### `method` 属性

### `fieldset`属性集


---

### 与本地js函数联动

点击按钮时，执行相应js函数

#####Example 1: `<input button>`

``` 
<input type="button" id="button1" onclick="button1_click();" value="button 1">
<script>
	function button1_click(){
		alert("clicked button1");
	}
</script>
```

#####Example 2: `button`

```
<button id="button1" onclick="button1_click();">button1</button>
<script>
	function button1_click(){
		alert("clicked button1");
	}
</script>
```

#####Example 3: 传递参数

```
<button id="button1" onclick="button1_click('hello');">button1</button>
<script>
function button1_click(s) {
	alert( s + " clicked");
}
</script>
```





