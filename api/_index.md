# kdXiaoyi.github.io API使用文档
如果您遇到了一些错误，也可以[在这里](https://kdxiaoyi.github.io/api/index.htm?help=1)自助排障
# What's API on kdXiaoyi.github.io?
为了完成亿些奇奇怪怪的操作，有时必须开发一些API来帮助个人网址建设。

您完全可以免费使用这些api！
# 主域API
这个API统一调用路径：`//kdXiaoyi.github.io/api/`

点击标题可以查看源码

其中`<>`的参数您必须提供，`[]`参数选择性提供


## [ifr](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/ifr.htm)
提供一个预览框架
```
ifr.htm
---
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
---
u= <VALUE>
back= [1]
```
### u
要跳转的URL
### back
如果为`1`，将会跳转后进行**一次**返回

这适用于：*e.g.* 当不识别MS-STORE链接时用[MS-STORE链接调用MSStore](http://kdxiaoyi.github.io/api/jump.htm?back=1&u=ms-windows-store://pdp/?ProductId=9WZDNCRFHVN5)

## [setCopiedBroad](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/copy.htm)
设置剪切板为一串文本
```
copy.htm
---
str= <value>
nback= [0|1]
tip= <value>
```
### str
要复制的文本
### nback
是否返回。
**为`1`时不返回**
### tip
提示信息。
默认`Copied!`，为`non`时不提示

## [Bilibili Vedio Player](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/bili_vedio.htm)
播放B站站内视频，请使用`iframe`调用。对于网页加参数修改iframe地址，请参阅[`ifr.htm`](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/ifr.htm)
```
bili_vedio.htm
---
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


## [Back](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/back.htm)
没有任何参数。调用后产生2次返回
```
back.htm
---
```


## [ms-office](https://github.com/kdXiaoyi/kdxiaoyi.github.io/blob/main/api/ms-office.htm)
调用Microsoft Office Web Client打开OFFICE文档
```
ms-office.htm
---
src= <Office Path>
```
### src
目标文档的网络路径，目前支持：[DOC](https://kdXiaoyi.github.io/api/ms-office.htm?src=//kdx233.github.io/res/docs/api_example/EXAMPLE.docx)/[PPT](https://kdXiaoyi.github.io/api/ms-office.htm?src=//kdx233.github.io/res/docs/api_example/EXAMPLE.pptx)/[XLS](https://kdXiaoyi.github.io/api/ms-office.htm?src=//kdx233.github.io/res/docs/api_example/EXAMPLE.xlsx)及其-X变种、模板变种、RTF文档

反正Microsoft Office 365 它都支持
