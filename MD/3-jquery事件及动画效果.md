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
### 二、鼠标移入移出事件
