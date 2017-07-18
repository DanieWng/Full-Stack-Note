# CSS 笔记

## 基础语法

css规则由两个主要的部分构成：

* 选择器
* 一条或多条声明

``` css
	selector {declaration1; declaration1; ... declarationN}
``` 

**选择器**通常是需要改变样式的html元素。

每条声明由一个属性和一个值组成。

属性是希望设置的样式属性。每个属性有一个值。属性和值被**冒号**分开。

```
	selector {property:value}
```

示例：

``` css
	h1{
		color:red;
		font-size:14px
	}
```

#### 注意点：

* 值的不同写法和单位
* 引号的使用(如果值为若干单词时，需要添加引号)
* 多重声明，需要用**分号**隔开
* 空格和大小写

## 高级语法

* **选择器的分组**

	```css
		h1,h2,h3,h4,h5,h6 {
	  		color: green;
	  	}
	```
	
* [**继承及其问题**](http://www.w3school.com.cn/css/css_syntax_pro.asp)

## 选择器

* [**派生选择器**](http://www.w3school.com.cn/css/css_syntax_descendant_selector.asp)

	派生选择器允许你根据文档的上下文关系来确定某个标签的样式。通过合理地使用派生选择器，我们可以使 HTML 代码变得更加整洁。
	
	```css
	li strong {
   		font-style: italic;
   		font-weight: normal;
  	}
	```
    示例中就是希望列表中的strong元素变为斜体字。
    
* [**id选择器**](http://www.w3school.com.cn/css/css_syntax_id_selector.asp)

	**id选择器**可以为标有特定id的HTML元素指定特定的样式。id选择器以`#`来定义。
	 
	``` html
	<p id="red">这个段落是红色。</p>
	<p id="green">这个段落是绿色。</p>
	```
	 
	``` css
	#red {color:red;}
	#green {color:green;}
```
	 
* [**id选择器和派生选择器**](http://www.w3school.com.cn/css/css_syntax_id_selector.asp)

	在现代布局中，id 选择器常常用于建立派生选择器。
	
	```css
	#sidebar p {
		font-style: italic;
		text-align: right;
		margin-top: 0.5em;
	}
	```
	
	上面的样式只会应用于出现在 id 是 sidebar 的元素内的段落。
	
	**一个选择器，多张用法**
	
	即使被标注为 sidebar 的元素只能在文档中出现一次，这个 id 选择器作为派生选择器也可以被使用很多次：
	
	```css
		#sidebar p {
			font-style: italic;
			text-align: right;
			margin-top: 0.5em;
		}

		#sidebar h2 {
			font-size: 1em;
			font-weight: normal;
			font-style: italic;
			margin: 0;
			line-height: 1.5;
			text-align: right;
		}
	```
	
	在这里，与页面中的其他 p 元素明显不同的是，sidebar 内的 p 元素得到了特殊的处理，同时，与页面中其他所有 h2 元素明显不同的是，sidebar 中的 h2 元素也得到了不同的特殊处理。
	
 	**单独的选择器**
 	
 	id 选择器即使不被用来创建派生选择器，它也可以独立发挥作用：
 	
 	```css
 	#sidebar {
		border: 1px dotted #000;
		padding: 10px;
	}
 	```
 	
 	根据这条规则，id 为 sidebar 的元素将拥有一个像素宽的黑色点状边框，同时其周围会有 10 个像素宽的内边距（padding，内部空白）
 	
 	> [ID 选择器详解](http://www.w3school.com.cn/css/css_selector_id.asp)
 
    
* [**类选择器**](http://www.w3school.com.cn/css/css_syntax_class_selector.asp)

	在 CSS 中，类选择器以一个点号显示：
	
	```css
	.center {
		text-align: center;
	}
	```
	
	* 和 id 一样，class 也可被用作派生选择器
	* 元素也可以基于它们的类而被选择

* [**属性选择器**](http://www.w3school.com.cn/css/css_syntax_attribute_selector.asp)

	对带有指定属性的 HTML 元素设置样式。
	可以为拥有指定属性的 HTML 元素设置样式，而不仅限于 class 和 id 属性。
	
	>只有在规定了 !DOCTYPE 时，IE7 和 IE8 才支持属性选择器。在 IE6 及更低的版本中，不支持属性选择。
	
	```
	# 为带有title属性的所有元素设置样式
	[title]
	{
		color:red;
	}
	
	# 为title="W3School"的所有元素设置样式
	[title=W3School]
	{
		border:5px solid blue;
	}
	```
	
	* **属性和值选择器 - 多个值**
	
		```
		# 为包含指定值的title属性的所有元素设置样式。
		[title~=hello] { color:red; }
		
		# 为带有包含指定值的lang属性的所有元素设置样式
		[lang|=en] { color:red; }
		```
		
	* **设置表单样式**
		
		属性选择器在为不带有 class 或 id 的表单设置样式时特别有用：
		

		```
		input[type="text"]
		{
		  width:150px;
		  display:block;
		  margin-bottom:10px;
		  background-color:yellow;
		  font-family: Verdana, Arial;
		}
		
		input[type="button"]
		{
		  width:120px;
		  margin-left:35px;
		  display:block;
		  font-family: Verdana, Arial;
		}
		```


	


