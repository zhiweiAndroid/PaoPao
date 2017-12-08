# PaoPao
Drawable 的使用

1.倒三角 泡提示的效果使用 9patch 来实现之外，还可以拿两个 Drawable 来拼接实现，这就需要一个圆角的矩形和一个三角的 Drawable

```
<!--倒三角的写法-->
<?xml version="1.0" encoding="utf-8"?>
<rotate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromDegrees="45"
    android:pivotX="135%"
    android:pivotY="15%"
    android:toDegrees="45"
    >
    <shape android:shape="rectangle">
        <solid android:color="#ffe39c"></solid>
    </shape>
</rotate>
<!--正三角的写法-->
<?xml version="1.0" encoding="utf-8"?>
<rotate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromDegrees="45"
    android:pivotX="-40%"
    android:pivotY="80%"
    android:toDegrees="45"
    >
    <shape android:shape="rectangle">
        <solid android:color="#ffe39c"></solid>
    </shape>
</rotate>
```

2.如何制作9.png

第一步：准备原图

将我们的图片放到drawable下面。

第二步：create 9patch图片

右键我们的图片选择create 9-Patch file...,选择存放的路径后，也就放在drawable下面然后确定，这个时候你会发现在drawable下面会出现一个popup_up.9.png 的图片。

第三步：对9patch图片处理

打开popup_up.9.png图片，会出现上图的界面，将我们的鼠标移到图片的四周会出现线，我们可以移动它给图片绘制1px宽度的黑线，左上两面绘制的黑线是设置可以拉伸的区域，右下是设置内容的区域，我们可以选中下面的show lock,show content,show patches,show bad patches这四个来看我们绘制后的效果。下面给出绘制后的效果图。

![img](http://img.blog.csdn.net/20151024140002880?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

