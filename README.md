# Carousel  原生js写的轮播
<br>Carousel使用

1 .引入css 和 js 文件:
<pre>
  link rel="stylesheet" type="text/css" href="carousel.css"
  script type="text/javascript" src="carousel.js"
</pre>

2 .html基本结构: 
元素嵌套结构: div>(div>div>img或者a)+div>左右切换按钮,id或者css选择器自定义.
例:<pre>
    \<div id="banner">
    \<div id="banner_img" class="banner_img">
      \<a href="###"><img src="" alt=""></a>
      \<a href="###"><img src="" alt=""></a>
      \<a href="###"><img src="" alt=""></a>
      \<a href="###"><img src="" alt=""></a>
    \</div>
    \<div class="btn">
      \<a href="###" class="prev"></a>
      \<a href="###" class="next"></a>
    \</div><br>
  \</div><br>
</pre>
3. Carousel初始化
<pre>
  Carousel("#banner","#banner_img",{prevBtn:".prev",nextBtn:".next",
        indexBtn:true,
   		//height:380,
        duration:40,
        autoPlay:true,
        autoPlayDir:"left",
        autoPlayTime:3000,
        actClass:"actClass",
        minWidth:"1024"
    });
/*第1个参数轮播容器选择器
第2个参数图片列表选择器
第3个参数
    {
		autoPlay//开启自动播放,默认不开启 ,
		height//轮播高度,默认380
    autoPlayTime//轮播间隔,默认1000
		autoPlayDir//轮播方向,默认'left'
		indexBtn//下标按钮选择器,默认false不显示,开启直接给选择器就行
		actClass//下标按钮选中样式
		prevBtn//左按钮选择器,默认.prev
		nextBtn//右按钮选择器,默认.next
		duration//动画过渡时长,默认40
		BezierCurve://贝赛尔曲线函数,默认ease
		minWidth//轮播最小宽度
	}
</pre>
