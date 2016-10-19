### 一、jquery动画效果
#### 示例代码 [动画](../HTML/cartoon.html)
``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin:0px;
			padding:0px;
		}
		.box{
			width: 300px;
			height: 300px;
			background-color: #f00;
		}
	</style>
</head>
<body>
	<input type="button" value="显示" id="show">
	<input type="button" value="隐藏" id="hide">
	<input type="button" value="切换" id="toggle">
	<input type="button" value="渐入" id="fadeIn">
	<input type="button" value="渐出" id="fadeOut">
	<input type="button" value="渐入渐出切换" id="fadeToggle">
	<input type="button" value="上卷" id="slideUp">
	<input type="button" value="下拉" id="slideDown">
	<input type="button" value="切换上卷下拉" id="slideToggle">
	<input type="button" value="动画" id="animate">
	<div class="box"></div>
	<script src="script/jquery.js"></script>
	<script>
		$("#show").click(function(){
			$(".box").show(5000);
		})
		$("#hide").click(function(){
			$(".box").hide(5000);
		})
		$("#toggle").click(function(){
			$(".box").toggle(5000);
		})

		$("#fadeIn").click(function(){
			$(".box").fadeIn(5000);
		})
		$("#fadeOut").click(function(){
			$(".box").fadeOut(5000);
		})
		$("#fadeToggle").click(function(){
			$(".box").fadeToggle(5000);
		})

		$("#slideUp").click(function(){
			$(".box").slideUp(5000);
		})
		$("#slideDown").click(function(){
			$(".box").slideDown(5000);
		})
		$("#slideToggle").click(function(){
			$(".box").slideToggle(5000);
		})

		$("#animate").click(function(){
			$(".box").animate({"margin-left":"200px","margin-top":"200px"},2000)
		})
	</script>
</body>
</html>
```
### 二、jquery事件

#### 鼠标移入移出事件
##### 示例代码 [mouse](../HTML/mouse.html)
``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin:0px;
			padding:0px;
		}
		.box{
			width: 300px;
			height: 300px;
			background-color: #f00;
		}
		.active{
			background-color: #00f;
		}
	</style>
</head>
<body>
	<div class="box"></div>
	<script src="script/jquery.js"></script>
	<script>
		$(".box").mouseenter(function(){
			$(this).addClass("active");
		});
		$(".box").mouseleave(function(){
			$(this).removeClass("active");
		});
	</script>
</body>
</html>
```
##### mouseover与mouseenter的区别
mouseenter() 方法 只有在鼠标指针经过被选元素时(不包括鼠标指针经过任何子元素)，才会触发 mouseenter 事件。mouseover ()方法在鼠标指针经过被选元素或者经过任何子元素时，都会触发 mouseover 。mouseleave事件 只有在鼠标指针离开被选元素时，才会触发 mouseleave 事件 。mouseout不论鼠标指针离开被选元素还是任何子元素，都会触发 mouseout 事件。

 示例代码 [区别](../HTML/over.html)
 ``` html
 <!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<p>不论鼠标指针穿过被选元素或其子元素，都会触发 mouseover 事件。</p>
	<p>只有在鼠标指针穿过被选元素时，才会触发 mouseenter 事件。</p>
	<div class="over" style="background-color:lightgray;padding:20px;width:40%;float:left">
		<h2 style="background-color:white;">被触发的 Mouseover 事件：<span></span></h2>
	</div>
	<div class="enter" style="background-color:lightgray;padding:20px;width:40%;float:right">
		<h2 style="background-color:white;">被触发的 Mouseenter 事件：<span></span></h2>
	</div>
	<script type="text/javascript" src="script/jquery.js"></script>
	<script type="text/javascript">
		x=0;
		y=0;
		$(document).ready(function(){
		  $("div.over").mouseover(function(){
		   	 	$(".over span").text(x+=1);
		  });
		  $("div.enter").mouseenter(function(){
		    $(".enter span").text(y+=1);
		  });
		});
	</script>
</body>
</html>
 ```
 
 #### 鼠标移入移出事件