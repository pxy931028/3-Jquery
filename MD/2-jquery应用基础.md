### 一、alert与console.log
alert与console.log不依赖jquery,是原生js的内容
+ alert()   		用于显示带有一条指定消息和一个 OK 按钮的警告框。
+ console.log() 	用于在控制台显示输出

#### 示例代码 [alert](../HTML/alert.html)
``` script
<script>
		alert("hello alert")
		console.log("hello console")
</script>
```
### 二、下载jquery
#### 下载node.js
+ 在百度搜索(node.js),下载并安装
+ 在git Base 中执行node -v 与 npm -v 查看版本
+ 执行 npm install jquery 命令下载jquery

#### 引入jquery的方法
jquery是用Javascript代码写好的功能库，而jquery.min.js是jquery压缩后的文件(传输过程中节省资源)。

``` script
<script src="script/jquery.js"></script>
```
### 三、选择器(css()方法改变元素样式)
单击相应的盒子使其由原来的红盒子变成蓝盒子

#### 示例代码 [$css](../HTML/$css.html)
``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		.box{
			width: 100px;
			height: 100px;
			background-color: #f00;
		}
	</style>
</head>
<body>
	<div class="box"></div>
	<div class="box"></div>
	<div class="box"></div>
	<script src="script/jquery.js"></script>
	<script>
		$(".box").click(function(){
			$(this).css("background-color","blue");
		})
	</script>
</body>
</html>
```
### 四、改变元素节点属性(attr()方法改变属性)
单击图片使其由原来的图片变换成另一张图片

#### 示例代码 [$attr](../HTML/$attr.html)
``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<img id="pic" src="images/1.jpg">
	<script src="script/jquery.js"></script>
	<script>

		$("#pic").click(function(){
			$(this).attr("src","images/2.jpg");
		});
	</script>
</body>
</html>
```
### 四、图片切换
+ index() 		返回指定元素相对于其他指定元素的 index 位置(找到元素的索引)
+ eq() 			将匹配元素集缩减值指定 index 上的一个(通过索引找元素)

#### 示例代码 [picture](../HTML/picture.html)
单击按钮可以切换到对应的图片并且按钮变为红色

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
		#list li{
			float:left;
			list-style:none;
			border:1px solid #aaa;
			width: 80px;
			height: 40px;
			line-height: 40px;
			text-align: center;	
			cursor: pointer;
			background-color: #fff;
		}
		#list .active{
			background-color: #f00;
		}
	</style>
</head>
<body>
	<img id="pic" src="images/0.jpg" alt="">
	<ul id="list">
		<li>1</li>
		<li>2</li>
		<li>3</li>
		<li>4</li>
		<li>5</li>
	</ul>
	<script src="script/jquery.js"></script>
	<script>
		$("#list li").click(function(){
			var i=$(this).index();				//	获取按钮的索引值
			var src="images/"+i+".jpg" ;     	//	获取索引对象
			$("#pic").attr("src",src);
			// $(this).css("background-color","#f00").siblings().css("background-color","#fff")
			$(this).addClass("active").siblings().removeClass("active");
		})
	</script>
</body>
</html>
```
#### 示例代码 [element](../HTML/element.html)
通过索引找元素
``` html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
	#myform input{
		margin-left:50px;
	}
    .box div{
       	width: 50px;
       	height: 50px;
       	border:1px solid red;
       	float:left;
       	margin-left:30px;
    }
	</style>
</head>
<body>
	<form id="myform" action="">
		<input type="button" value="1">
		<input type="button" value="2">
		<input type="button" value="3">
	</form>
	<div class="box">
		<div></div>
		<div></div>
		<div></div>
	</div>
	<script src="script/jquery.js"></script>    
   <script>
        $("#myform input").click(function(){
            var index = $(this).index();
        	$(".box div").eq(index).css("background-color","red").siblings().css("background-color","#fff");
        })
   </script>
</body>
</html>
```
### 五、选项卡制作
#### 示例代码 [selector](../HTML/selector.html)
单击选项卡切换到不同的内容中
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
			box-sizing:border-box;
		}
		.clearFix:before,.clearFix:after{
			content:"";
			display:block;
			clear:both;
		}
		.list li{
			float:left;
			list-style:none;
			width: 100px;
			height: 40px;
			line-height: 40px;
			text-align:center;
			border:1px solid #aaa;
			cursor: pointer;
		}
		.content div{
			width: 300px;
			height: 300px;
			border:1px solid red;
			display:none;
		}
		.content .active{
			display:block;
		}
	</style>
</head>
<body>
	<ul class="list clearFix">
		<li>选项一</li>
		<li>选项二</li>
		<li>选项三</li>
	</ul>
	<div class="content">
		<div class="active"><h1>内容一</h1></div>
		<div><h1>内容二</h1></div>
		<div><h1>内容三</h1></div>
	</div>
	<script src="script/jquery.js"></script>
	<script>
		$(".list li").click(function(){
			var i=$(this).index();
			$(".content div").eq(i).addClass("active").siblings().removeClass("active");
		})
	</script>
</body>
</html>
```