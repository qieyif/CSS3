# CSS3之动画(*Animation*)

> - CSS3动画，能在网页中取代动画图片GIF、Flash、以及javascript。
> - CSS3核心关键字是@keyframes,定义动画。
> - 高级浏览器支持CSS3动画。
> - CSS3的animation属性可以像Flash制作动画一样，通过控制关键帧来控制动画的每一步，实现更为复杂的动画效果。


##### ainimation实现动画效果主要由两部分组成：
	1）通过类似Flash动画中的帧来声明一个动画；
	2）在animation属性中调用关键帧声明的动画。

##### animation属性：
| 属性 | 描述 |
|--------|--------|
|    animation-name    | 用来指定关键帧动画的名字       |
|    animation-duration    | 用来指定动画播放所需的时间，以s为单位       |
|    animation-timing-function    | 设置动画的播放方式       |
|    animation-delay    | 指定动画开始的时间，以s为单位       |
|    animation-iteration-count    | 指定动画播放的次数       |
|    animation-direction    | 控制动画的播放方向       |
|    animation-play-state    | 设置动画的播放状态，播放还是暂停       |
|    animation-fill-mode    | 设置动画的时间外属性       |

---

- ***animation-name***：none为默认值，将没有任何动画效果，其可以用来覆盖任何动画 
- ***animation-duration***：默认值为0，意味着动画周期为0，也就是没有任何动画效果 
- ***animation-timing-function***：与transition-timing-function一样 
- ***animation-delay***：在开始执行动画时需要等待的时间 
- ***animation-iteration-count***：定义动画的播放次数，默认为1，如果为infinite，则无限次循环播放 
- ***animation-direction***：默认为nomal，每次循环都是向前播放，（0-100），另一个值为alternate，动画播放为偶数次则向前播放，如果为基数词就反方向播放
- ***animation-state***：默认为running，播放，paused，暂停 
- ***animation-fill-mode***：定义动画开始之前和结束之后发生的操作，默认值为none，动画结束时回到动画没开始时的状态；forwards，动画结束后继续应用最后关键帧的位置，即保存在结束状态；backwards，让动画回到第一帧的状态；both：轮流应用forwards和backwards规则。

---

`实例如下：`
```
	/*demo1*/
	.demo1{
		background: #556B2F;
	}
	.demo1:hover{
		animation: demo1 5s ease 3s 2 alternate;
	}
	/*定义动画demo1*/
	@keyframes demo1{
		0% {
			background: #666666;
		}
		25%{
			background: #FF0000;
		}
		50% {
			background: #B8860B;
		}
		100% {
			background: #0000FF;
		}
	}
```

---
#### animation复合属性：

	animation: animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count,animation-direction;
	
	example: 
	
		animation: ani1, 5s, ease, 2s, 2, alternate;
	
	
##### animation和transition的区别：
- animation属性类似于transition，他们都是随着时间改变元素的属性值。
- transition需要触发一个事件才会随着时间改变其css属性，而animation在不需要触发任何事件的情况下，也可以实现。
