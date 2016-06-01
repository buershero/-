# 前端页面制作规范


页面制作规范 html css

---

## 目的
编写灵活、稳定、高质量的代码，推进代码的可维护性和可读性、方便后期的管理和维护。尽量保持统一的编写风格。
## HTML
### 基本规则
> * 用两个空格来代替制表符（tab） 嵌套元素缩进一次（即两个空格）
> * 对于属性的定义，确保全部使用双引号，自闭合元素的尾部不用添加斜线 --HTML5 规范中明确说明这是可选的。
> * <meta name="renderer" content="webkit">
> * <meta charset="UTF-8"> 确保浏览器快速并容易的判断页面内容的渲染方式。
> * 省略引入 CSS 和 JavaScript 文件时 type 属性，因为 text/css 和 text/javascript 分别是它们的默认值。
> * 布尔型属性不需要赋值，XHTML 规范要求为其赋值，但是 HTML5 规范不需要。
> * 尽量遵循 HTML 标准和语义，尽量使用最少的标签并保持最小的复杂度。

### 基本模板
```html
<!doctype html>
<!--[if lt IE 7 ]><html class="ie6" lang="zh-cn"><![endif]-->
<!--[if IE 7 ]><html class="ie7" lang="zh-cn"><![endif]-->
<!--[if IE 8 ]><html class="ie8" lang="zh-cn"><![endif]-->
<!--[if IE 9 ]><html class="ie9" lang="zh-cn"><![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--><html class="" lang="zh-cn"><!--<![endif]-->
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="renderer" content="webkit">
    <title>Title</title>
 
  </head>
  <body>
  </body>
</html>
```

<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
其中http-equiv=”X-UA-Compatible”这个是IE8的专用标记，是用来指定Internet Explorer 8 浏览器模拟某个特定版本IE浏览器的渲染方式，以此来解决IE浏览器的兼容问题。如果系统安装ie8或以上版本，则使用最高版本ie渲染；否则，这个设定可以忽略。

### HTML注释

```html
<!-- 播放器模块[[ -->
<div class="video-box">
……
</div>
<!-- 播放器模块]] -->
```

## CSS
###基本规则
> * 为选择器分组时，将单独的选择器单独放在一行。
> * 为了代码的易读性，在每个声明块的左花括号前添加一个空格，声明块的右花括号应当单独成行。
> * 每条声明语句的冒号（:） 后插入一个空格。为了获得更准确的错误报告，每条声明都应该独占一行。
> * 所有声明语句都应当以分号结尾。
> * 十六进制值应该全部小写，尽量使用简写形式的十六进制值，例如，用 #fff 代替#ffffff。
> * 避免为 0 值指定单位，用 margin: 0; 代替margin: 0px;。
> * 带前缀的属性，让属性的值对齐便于编辑（或者用工具自动添加前缀？）
> * 为了易读性和便于快速编辑，将单条声明的语句放在同一行。
> * 避免过度使用简写，容易对属性值带来不必要的覆盖、引起意外的副作用。

### class 命名
> * class 名称中只能出现小写字符和破折号（dashe）（不是下划线，也不是驼峰命名法）。破折号应当用于相关 class 的命名（类似于命名空间）（例如，.btn 和 .btn-danger）。
> * 避免过度任意的简写。.btn 代表 button，但是 .s 不能表达任何意思。
> * class 名称应当尽可能短，使用有组织的或目的明确的名称。
> * 基于最近的父 class 或基本（base） class 作为新 class 的前缀。

### 常用CSS命名

| 中文名        | 建议class   | 中文名        | 建议class   | 
| --------   | -----:  | 
|头部	|header	|外围容器|	wrapper|
|尾部	|footer	|容器	|container|
|内容	|content|	页面主体|	main|
|导航	|nav	|栏目/列|	column|
|顶导航	|topnav|	菜单|	menu|
|子导航	|subnav|	侧栏|	sidebar|
|子菜单	|submenu|	模块|	module|
|标题	|title|	标签页|	tab|
|提示	|tips|	状态|	status|
|当前	|current	|按钮|	btn|
|摘要	|summary	|滚动|	scroll|
|下拉	|dropdown	|搜索|	search|
|标志	|logo|
|广告	|banner|
|登陆	|login|
|登录条	|login-bar|
|注册|	reg|
|加入	|join|
|面包屑	|crumbs|
|分页	|pagination|
|状态	|status|
|按钮	|btn|
|弹出层	|pop|
|设置	|set|
|添加	|add|
|滚动	|scroll|
|删除	|del|
|操作	|op|
|密码	|pwd|
|导入	|inc|
|标签页	|tab|
|文章列表	|list|
|提示信息	|msg|
|小技巧	|tips|
|图标	|icon|
|注释	|note|
|指南	|guide|
|服务	|service|
|热点	|hot|
|新闻	|news|
|下载	|download|
|投票	|vote|
|合作伙伴	|partner|
|版权	|copy-right|
|友情链接	|link|
|提示信息	|info|
|成功	|success|
|报错|	error|
|警告|	warning|

> * 建议命名时尽量规避"ad"、"ads"、""advertisement"等含广告、推广意思的词，减少因去广告插件或国内山寨浏览器“优化”导致的问题。

## 声明顺序
> * 显示、位置属性
display, position, left, top, float, clear, list-style
> * 盒模型
width, height, margin, padding, border
> * 背景、行高
background,line-height
> * 文本属性
color, font, text-decoration, text-align, text-indent, vertical-align, white-space,word-wrap,word-break
> * 其它
cursor, z-index, zoom，opacity
> * css3
transform, transition, animation, box-shadow, border-radius
> * hack （统一用csshack）

```html
<!--[if lt IE 7 ]><html class="ie6" lang="zh-cn"><![endif]-->
<!--[if IE 7 ]><html class="ie7" lang="zh-cn"><![endif]-->
<!--[if IE 8 ]><html class="ie8" lang="zh-cn"><![endif]-->
<!--[if IE 9 ]><html class="ie9" lang="zh-cn"><![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--><html class="" lang="zh-cn"><!--<![endif]-->
```

##注释
文件顶部注释(多行)
```
/* 文件内容简要描述 */
```

模块注释（单行）
```
/* 模块名称 */
```

特殊注释，用于标注代办、修改等信息
```
/* BUGFIX: xxxx */
```
其它
```
简明扼要。为避免极端情况下出现乱码字符导致注释范围意外扩大，注释的星号与内容之间有一个空格。
```

##代码组织 （PS:统一即可，非必要）
> 以组件为单位组织代码段






