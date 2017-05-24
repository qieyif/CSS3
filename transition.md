# CSS3之过渡(*transition*)

> CSS3过渡使用的css属性是***transition***。
> 通过CSS3过渡，我们可以实现元素从一种样式变换到另外一种样式的效果。
> ***transition*** 一般高级浏览器都支持。

---
#### Transition 过渡

| 属性 |描述|
|:--------:|:--------|
|    transition    | 复合属性。检索或设置对象变换时的过渡效果    |
|    transition-property    | 检索或设置对象中参与过渡的属性    |
|    transition-duration    | 检索或设置对象过渡的持续时间    |
|    transition-timing-function    | 检索或设置对象中过渡的类型 |
|    transition-delay    | 检索或设置对象延迟过渡的时间  |

---
- ***transition*** 过渡的复合属性。` transiton : 过渡属性 过渡所需要时间 过渡动画函数 过渡延迟时间`。
- ***transition-property*** 设置的要参与过渡的属性 例如：width height border color background-color transform 等。
- ***transition-duration*** 设置过渡的时间，过渡所需要花费的时间。单位是s。

`示例如下 ： 红色的方块会在2s的时间内过渡到蓝色，视觉上是一种动画的效果。`

``` css
	div{
		width: 200px;
		height: 200px;
		background-color: #f00;
		transition-property: background-color;
		transition-duration: 2s;
	   }
  div:hover{
		background-color: #00f;
	   }

```

- ***transition-timing-function*** 指定过渡的函数 `liner:匀速；ease-in：减速；ease-out：加速；ease-in-out:先加速再减速；cubic-bezier:三次贝塞尔曲线 可以定制` [跳转到cubic-bezier定制页面](http://cubic-bezier.com/#.06,.88,.84,.24)
- ***transition-delay*** 过渡延迟时间

[点击查看过渡的小例子](https://github.com/qieyif/Learn-CSS/blob/master/transition.html)
---
##### 触发过渡的条件
> 单纯的代码并不能触发任何的过渡效果，需要用户的行为，例如点击，划过等事件进行触发，可以触发的方式如下“

```css
    :hover
    :focus
    :checked
    click
    javascript触发
    媒体查询触发
    ...
```

##### 过渡的局限性

- transition的优点就是简单易用，但是有几个大的局限性，已至于大多数情况下需要使用css3的动画。
- transition需要事件触发，所以没办法再网页加载时自动触发。
- transition是一次性的，不能重复发生，除非一再出发。
- transition只能定义开始状态和结束状态，不能定义中间状态，也就是说只有两个状态。所以要想描述元素变化的期间的多个状态，需要用动画。
- 一个transition规则只能定义一个属性的变化，不能涉及多个属性。

---

**css3的Animation动画就是为了解决这些问题出现的**[跳转到CSS3-Animation动画教程]()

