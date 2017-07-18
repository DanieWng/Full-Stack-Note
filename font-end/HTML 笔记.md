# HTML 笔记

## head

1. <h3>meta 标签</h3>

	> [meta标签详解](http://www.jianshu.com/p/36d94ba7c63b)
	
		
	``` html
	<head>
		<meta charset="utf-8">
		<mata http-equiv="X-UA-Compatible" content="IE=edge">
	</head>
		
	```
	
	##### 主要属性类别：
	
	1. ##### name属性
		
		主要用于描述网页。
		
		
	2. ##### http-equiv属性
	
		类似于HTTP的头部协议，回应给浏览器一些有用的信息，帮助正确和精确地显示网页内容。
		
2. <h3>style 标签</h3>

	**\<style>**标签用于为HTML文档定义样式信息。

	* type属性是必须的，定义style元素的内容，唯一可能的值是**"text/css"**
	* style元素位于**head**标签内
	* 需要链接外部样式表，请使用[**\<link>标签**](http://www.w3school.com.cn/tags/tag_link.asp)
	* [css教程](http://www.w3school.com.cn/css/index.asp)

## body

## form

```
<form>
...
</form>
```

一般用于用户输入的区块

* **input** 元素
	* `<input type="text">` 定义一个文本输入框
	* `<input type="radio">` 定义一个radio按钮（多选一）
	* `<inout type="submit">` 定义一个提交按钮

* `action` 属性

* `method` 属性

* `fieldset`属性集

#### 与本地js函数联动

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

## 

