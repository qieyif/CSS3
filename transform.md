# CSS3之变换（*Transform*）

> - transform 属性向元素 应用 2D 或 3D 转换。
> - 该属性允许我们对元素进行 ***旋转***、***缩放***、***移动***、***倾斜***。

##### transform语法：

```css
	transform: none|transform-functions;
```

#### Transform 2D转换：

| transform的值 |   描述   |
| :--------:   |---|
| translate()  |移动|
| rotate()  |旋转角度|
| scale()  |缩放比例|
| skew()  |倾斜、拉伸|
| matix()  |matrix() 方法把所有 2D 转换方法组合在一起。共6个参数。|

---
`实例demo1如下：`

```css
css:
	div{
        width: 200px;
        height: 200px;
        line-height: 200px;
        text-align: center;
    }
    /*demo1*/
    .demo1{
        background-color: #B8860B;
        transform: rotate(60deg);
    }

html:
    <body>
        <div class="demo1">Demo1</div>
    </body>

```
`注释：这个div矩形 会顺时针旋转60度。`

---
`实例demo2如下：`
```css
css:
	/*.demo2*/
    .demo2{
        background: #556B2F;
        transform: translate(200px,200px);
    }
```
`注释：这个div矩形 会向右移动200px，向下移动300px。 右和下是translate正方向！`

---
`实例demo3如下：`
```css
css:
	/*demo3*/
    .demo3{
        background-color: #B8860B;
        transform: scale(1.5);
    }
```
`注释：这个div矩形 会缩放到原来的1.5倍大小！`

---
`实例demo4如下：`

```css
	/*demo4*/
    .demo4{
        background-color: #666666;
        transform: skew(-45deg);
    }
```
`注释：这个div矩形 会倾斜、拉伸45度！`

---
##### transform-origin：
- transform-origin 属性允许您改变被转换元素的位置。
- 默认值 50% 50%； 效果相当于 center center；

| 可以取值 | 描述 |
|--------|--------|
|   left     |    指定原点的横坐标为left    |
|   center     |    指定原点的横坐标为center  |
|   right     |    指定原点的横坐标为right   |
|   top     |    指定原点的纵坐标为top    |
|   center     |    指定原点的纵坐标为center  |
|   bottom     |    指定原点的纵坐标为bottom  |

---

#### Transform 3D转换：

##### transform-style：
```css
	transform-style：flat | preserve-3d
```
- **flag :** 指定子元素位于此元素所在平面内。
- ** preserve-3d：** 指定子元素定位在三维空间内。

`说明： 指定某元素的子元素是（看起来）位于三维空间内，还是在该元素所在的平面内被扁平化。决定一个变换元素看起来是处在三维空间还是平面内，需要该元素的父元素上定义 <' transform-style '> 属性。`

---



