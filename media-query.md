# CSS3之媒体查询

> - 媒体查询的核心是使用 ***@media*** 关键字。
> - @media 可以针对不同的屏幕尺寸设置不同的样式，特别是如果你需要设置设计响应式的页面，***@media*** 是非常有用的。
> - 当你重置浏览器大小的过程中，页面也会根据浏览器的宽度和高度重新渲染页面。
> - 媒体查询让CSS可以更精确作用于不同的媒体类型和同一媒体的不同条件。
> - 媒体查询的大部分媒体特性都接受min和max用于表达“大于或等于”和“小与或等于”。如：width会有min-width和max-width。
> - 媒体查询可以被用在CSS中的 ***@media*** 和 ***@import*** 规则上，也可以被用在HTML和XML中。

### 各大浏览器的支持程度如下：

| Chrome | IE |FireFox | Safari | Opera |
|:--------:|--------|:--------:|--------|:--------:|
|    13    |    9   |    10.0    |  6.1    |     15  |

---

### 媒体查询的语法：


`第一种语法：直接在link中判断设备的尺寸，引用不同的css文件：`

```css
	<link rel="stylesheet" media="mediatype and|not|only (media feature)" href="demo.css">

```

`第二种语法：直接写在style标签里或者css文件当中：`

```css
	@media mediatype and|not|only (media feature) {
    	CSS-Code;
	}

```
---
##### 举例如下：

```css
	<link rel="stylesheet" type="text/css" href="demo.css" media="screen and (min-width: 768px)">
```
> 这句意思是：设备屏幕的宽度只要是大于或者等于768px，就会引入demo.css文件，如果设备的屏幕宽度小于768px，就不会引入这个css文件。


```css
    @media screen and (max-width: 992px) {
      body {
        background: #ccc;
      }
    }
```
> 这句意思是： 设备的屏幕小于或者等于992px，body的背景颜色就会设置成灰色，如果设备的屏幕大于992px，body不会设置成灰色，这句代码不会起作用。

---
### 媒体类型

| 媒体类型 |描述|
|:--------:|:--------:|
|    all    | 用于所有设备      |
|    print  | 用于打印机和打印预览|
|    screen | 用于电脑屏幕，平板电脑，只能手机等|

### 媒体查询中的 ***not*** ***only*** ***all*** 等关键字
| 关键字 |描述|
|:--------:|:--------:|
|    all  | 用于所有设备      |
|    not  | 用来排除掉某些特定的设备的。比如 @media not print（非打印设备）|
|    only | 用来定某种特别的媒体类型。 比如 @media only screen|

### 媒体特性 (*Media Features*)：

| 媒体特性 |
|:--------:|
|    width    |
|    height    |
|    device-width    |
|    device-height    |
|    aspect-ratio    |
|    device-aspect-ratio    |
|    color    |
|    color-index   |
|    monochrome   |
|    resolution   |
|    scan   |
|    grid   |

---

###### width: 分为min-width 和 max-width两个媒体特性：

```css
	<link media="screen and (min-width:400px) and (max-width:900px)" rel="stylesheet" href="example.css" />
```
> 代码含义： 只有设备屏幕大于400px而且小于900px之间，才会引入这个css文件。

---


