#ImageMagick 命令

#拼接图片

#剪裁图片
* 分隔多张小图

* 剪裁一张指定尺寸的小图
	1.	在原始图片的上距离上部30像素左部50为起点的位置，分别向左向下截取一块100x80的图片，如果x相对坐标不足100，那么取实际值。
	```
	convert src.jpg -crop 100x80+50+30 dest.jpg
	```
	2.	在原始图片截取中心部分一块100x80的图片
	```
	convert src.jpg -gravity center -crop 100x80+0+0 dest.jpg
	```
	3.	在原始图上截取右下角距离下边缘10个像素，右边缘5像素一块100x80的图片
	```
	convet src.jpg -gravity southeast -crop 100x80+10+5 dest.jpg
	```
	
	```
	// 左上角
	convert scr.png -crop 36x36+0+0 dest.png
	
	// 右上角
	convert scr.png -gravity northeast -crop 36x36+0+0 dest.png
	
	// 右下角
	convert scr.png -gravity southeast -crop 36x36+0+0 dest.png
	
	// 左下角
	convert scr.png -gravity southwest -crop 36x36+0+0 dest.png
	
	// 中间
	convert scr.png -gravity center -crop 36x36+0+0 dest.png
	```
