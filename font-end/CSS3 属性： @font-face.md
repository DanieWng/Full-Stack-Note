# CSS3 属性： @font-face

**\<style>**标签用于为HTML文档定义样式信息。

* type属性是必须的，定义style元素的内容，唯一可能的值是**"text/css"**
* style元素位于**head**标签内
* 需要链接外部样式表，请使用[**\<link>标签**](http://www.w3school.com.cn/tags/tag_link.asp)
* [css教程](http://www.w3school.com.cn/css/index.asp)


## @font-face

在网页中插入特殊字体, 是css3中的一个模块。 

``` css
@font-face {
  font-family: <YourWebFontName>;
  src: <source> [<format>][,<source> [<format>]]*;
  [font-weight: <weight>];
  [font-style: <style>];
}
```

**YourWebFontName**：自定义的字体名称，最好是使用你下载的默认字体，他将被引用到你的Web元素中的font-family。如font-family:"YourWebFontName";

**src**：设置字体的加载路径和格式，通过逗号分隔多个加载路径和格式；

**src**：还有一个属性local(font name)字段，表示从用户系统中加载字体，失败后才加载webfont

`src:local(font name), url('font_name.ttf')`

source：字体的存放路径，可以是相对路径也可以是绝路径；

format：自定义的字体的格式，主要用来帮助浏览器识别，其值主要有以下几种类型：

truetype,opentype,truetype-aat,embedded-opentype,svg等；

weight：定义字体是否为粗体；

style：定义字体样式，如斜体；


> [CSS3 @font-face](http://www.jianshu.com/p/0fbfc692f5ff)
