
# canvas-dmeo
有关canvas相关demo


# canvas倒计时

> canvas开始是一个空白，为了展示首先需要渲染

##### 栅格
> canvas默认被网格覆盖，一个单元格相当于一个像素，栅格的起点为左上角（坐标为（0,0））。所有元素的位置都相对于原点定位。所以图中蓝色方形左上角的坐标为距离左边（X轴）x像素，距离上边（Y轴）y像素（坐标为（x,y））![](img/Canvas_default_grid.png)

1.getContext()--用来渲染上下文和绘画功能。只有一个参数-》文件的格式2d,3d;不建议使用样式指定画布大小，因为画布的大小不单单是指画布的大小，还是里面像素的大小
``

2.绘制图形：

> 1.长方形：</br>
       canvas提供了三种方法绘制矩形：

       fillRect(x, y, width, height)
       绘制一个填充的矩形
       strokeRect(x, y, width, height)
       绘制一个矩形的边框
       clearRect(x, y, width, height)
       清除指定矩形区域，让清除部分完全透明

   2.绘制路径：

     路径绘制图形的步骤
      1.首先，你需要创建路径起始点。
      2.后你使用画图命令去画出路径。
      3.之后你把路径封闭。
      4.一旦路径生成，你就能通过描边或填充路径区域来渲染图形。

     画图命令：
     beginPath()：新建一条路径，生成之后，图形绘制命令被指向到路径上生成路径-》再设置起始位置，moveTo(x,y);
     closePath()：闭合路径之后图形绘制命令又重新指向到上下文中
     stroke()：线条绘制轮廓
     fill()：填充路径内容生成实心内容

   3.绘制圆或者弧形

     1.beginPath();新建路径
     2.arc(x,y,半径，起始角度，结束角度，绘画方向)//绘画方向：false顺时针，true逆时针=====起始角度/结束角度：指的是弧度，而不是确切的角度；弧度=radians=(Math.PI/180)*旋转角度；x,y代表圆心位置
     3.moveTo(x,y):移动哪里开始

   4.二次贝塞尔曲线及三次贝塞尔曲线

     quadraticCurveTo(cp1x, cp1y, x, y)
     绘制二次贝塞尔曲线，cp1x,cp1y为一个控制点，x,y为结束点。
     bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
     绘制三次贝塞尔曲线，cp1x,cp1y为控制点一，cp2x,cp2y为控制点二，x,y为结束点

