# 撕裂Bitmap吧！

一直以来，我们使用Android的Bitmap的时候，一度将其放置在view当中，可当view发生改变之后，它却是"好动分子"，可总有一些需求是希望它能"无动于衷"。就好比下面这种情况

![](https://github.com/liuzhushaonian/SlitBitmap/blob/master/screen_short/slit.gif)

这个功能我最早发现只有Android官方在使用，就隐藏在媒体通知栏上，在其向上折叠的时候，背景图并未跟着折叠变形，而是保持不动，让我一下子对这个效果产生了兴趣，可一时间也搞不懂要怎样做。

之后在做lin15的时候，下拉快速设置面板的背景动画实在不好看，我的脑子里一瞬间就想到了这个效果。

## 已实现功能：

根据外部传入的limit对Bitmap进行不同程度的裁剪绘制，使之产生卷轴滚动展开图片的效果。

- 支持drawable
- 支持上下左右四个方向的展示，但一次仅能实现一个方向的展示。
- 支持设置透明度
- 支持


## 使用方法：

- setExpand(int expand) //设置展开方向

- setAlpha(int alpha) //设置透明度（0~255）

- change(int limit) //改变展示尺寸，主要方法


外部传入limit，决定好展开方向后，即可不断调用change方法展示Bitmap，如上图所示。


