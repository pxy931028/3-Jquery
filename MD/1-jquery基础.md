### jQuery入门基础
#### 一、js与jquery关系
+  js(javaScript)是世界上最流行的脚本语言，因为你在电脑、手机、平板上浏览的所有网页，以及无数基于HTML5的手机APP，交互逻辑都是由Javascript驱动的。简单来说，Javascript是一种运行在浏览器中的解释型的编程语言。(在web世界里，只有js能跨平台，跨浏览器驱动网页与用户交互)
+  jquery是一个兼容多浏览器的js框架，jquery极大的简化了js编程，语法简单，易用，容易上手。它实际上是一种逻辑式语言和纯粹的函数式语言的结合体，比js更加方便地控制页面，查询。
+  jQuery 是一个“写的更少，但做的更多”的轻量级 JavaScript 库。是继Prototype之后的又一个优秀的javascript库。jquery，顾名思义，也就是javascript和查询(Query),即是辅助javascript开发的库。

#### 二、jquery选择器  $()
##### $的作用
+ $("选择器")          jquery选择器
+ $("<img>")  		   创建一个jquery对象(标签)
+ $(this) 			   把另一个对象变成jquery对象

#### 三、jquery事件
    jQuery 事件处理方法是 jQuery 中的核心函数。事件处理程序指的是当 HTML 中发生某些事件时所调用的方法。

+ $(document).ready(function) 		将函数绑定到文档的就绪事件（当文档完成加载时） 
+ $(selector).click(function) 		触发或将函数绑定到被选元素的点击事件 
+ $(selector).dblclick(function) 	触发或将函数绑定到被选元素的双击事件 
+ $(selector).focus(function) 		触发或将函数绑定到被选元素的获得焦点事件 
+ $(selector).blur(function) 		触发或将函数绑定到被选元素的失去焦点事件 
+ $(selector).mouseover(function) 	触发或将函数绑定到被选元素的鼠标悬停事件 
+ $(selector).mouseout(function) 	触发或将函数绑定到被选元素的鼠标悬停事件 
+ $(selector).mouseenter(function) 	鼠标移动到元素上方时触发事件
+ $(selector).mouseleave(function) 	鼠标离开元素时触发事件

##### jquery事件的坐标属性
相对于整个文档中的坐标（文档绝对坐标） 
+ event.pageX 		相对于文档左边缘的鼠标位置。 
+ event.pageY 		相对于文档上边缘的鼠标位置。 


#### 四、jquery方法
##### 属性操作
+ addClass() 		向匹配的元素添加指定的类名。 
+ attr() 			设置或返回匹配元素的属性和值。 
+ hasClass() 		检查匹配的元素是否拥有指定的类。 
+ html() 			设置或返回匹配的元素集合中的 HTML 内容。 
+ removeAttr() 		从所有匹配的元素中移除指定的属性。 
+ removeClass() 	从所有匹配的元素中删除全部或者指定的类。 
+ toggleClass() 	从匹配的元素中添加或删除一个类。 
+ val() 			设置或返回匹配元素的值。 

##### 获取节点(子级，父级，同级，过滤)
+ find() 			返回被选元素的后代元素，一路向下直到最后一个后代。
+ children() 		返回被选元素的所有直接子元素。

+ parent() 			返回被选元素的直接父元素。
+ parents() 		返回被选元素的所有祖先元素，它一路向上直到文档的根元素 (<html>)。
+ parentsUntil() 	返回介于两个给定元素之间的所有祖先元素。

+ sibling() 		返回被选元素的所有同胞元素。
+ next() 			返回被选元素的下一个同胞元素。
+ nextAll() 		返回被选元素的所有跟随的同胞元素。
+ nextUntil() 		返回介于两个给定参数之间的所有跟随的同胞元素。

+ first() 			返回被选元素的首个元素。
+ last() 			返回被选元素的最后一个元素。
+ eq() 				返回被选元素中带有指定索引号的元素。
+ filter() 			允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。
+ not() 			返回不匹配标准的所有元素。

##### 节点操作
+ append()  	在被选元素的结尾插入内容
+ prepend()  	在被选元素的开头插入内容
+ after() 		在被选元素之后插入内容
+ before()  	在被选元素之前插入内容
+ remove()  	删除被选元素（及其子元素）
+ empty()  		从被选元素中删除子元素


#####  动画效果
+ hide() 		用于隐藏 HTML 元素
+ show() 		用于显示 HTML 元素
+ toggle() 		可以在 hide() 和 show() 方法之间进行切换
+ fadeIn() 		用于淡入已隐藏的元素
+ fadeOut() 	用于淡出可见元素
+ fadeToggle() 	可以在 fadeIn() 与 fadeOut() 方法之间进行切换
+ fadeTo() 		允许渐变为给定的不透明度（值介于 0 与 1 之间）
+ slideDown() 	用于向下滑动元素
+ slideUp() 	用于向上滑动元素
+ slideToggle() 可以在 slideDown() 与 slideUp() 方法之间进行切换
+ animate() 	用于创建自定义动画
+ stop() 		用于在动画或效果完成前对它们进行停止





	


