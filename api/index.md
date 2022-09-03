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