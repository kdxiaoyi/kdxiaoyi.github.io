# kdXiaoyi.github.io API使用文档
# What's API on kdXiaoyi.github.io?
为了完成亿些奇奇怪怪的操作，有时必须开发一些API来帮助个人网址建设。

您完全可以免费使用这些api！
# API LIST
API统一调用路径：`//kdXiaoyi.github.io/api/`

点击标题可以查看源码

其中`<>`的参数您必须提供，`[]`参数选择性提供
## [frame](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/frame.htm) **未实现**
提供一个预览框架
```
frame.htm
url= <VALUE>
goto= [f]
```
### url
提供一个要预览的URL
### goto 
如果为`f`，将不允许用户前往此URL
## [jump](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/jump.htm)
提供一个跳转通道
```
jump.htm
u= <VALUE>
back= [1]
```
### u
要跳转的URL
### back
如果为`1`，将会跳转后进行**一次**返回

这适用于：*e.g.* 当不识别MS-STORE链接时用[MS-STORE链接调用MSStore](http://kdxiaoyi.github.io/api/jump.htm?back=1&u=ms-windows-store://pdp/?ProductId=9WZDNCRFHVN5)
## [Bilibili Vedio Player](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/bili_vedio.htm)
播放B站站内视频，请使用`iframe`调用
```
bili_vedio.htm
dm= [0|1]
av= <value>
bv= <value>
p= [Int]
```
*e.g.* [HERE](//kdXiaoyi.github.io/api/bili_vedio.htm?dm=1&av=386414259&bv=BV1Ad4y1U7Ad&p=1)
### dm
控制是否启用弹幕。`1`为启用，也为默认
### av & bv
至少提供一个。

av格式：`一串数字`

bv格式：`BVxxxxxxx`

获取方式：
```
AV：视频分享选择嵌入链接，从得到的HTML中avid后面值找到。或者AV视频看视频URL
BV：通常在URL后面有
```
### p
提供一个整数。如果对于多P视频则有效，否则为`1`。