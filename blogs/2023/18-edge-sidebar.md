# 18# 一键禁用Edge的Bing Discover (Sidebar)
<small><a href="../">←返回</a> | 创建：2023-03-18 | 最后更新：2023-03-18</small> | <a href="https://www.bilibili.com/read/cv22481259">在Bilibili上查看 ></a> | <a href="https://zhuanlan.zhihu.com/p/614999864">在知乎上查看 ></a><br>

# 方式1
[工具下载页](/disabled-edge-sidebar/)

# 方式2
### 修改启动增强
首先，请在`edge://settings/system`中关闭`启动增强`和下面的`在 Microsoft Edge 关闭后继续运行后台扩展和应用`<br>

### 不修改启动增强
如果您需要启动增强：**或者**找到注册表`HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`，找到`MicrosoftEdgeAutoLaunch`，在值的**最后面**加上` --disable-features=msUndersideButton`<br>
注意，`--`前面有个空格

## 后续操作

右键桌面的edge快捷方式，在“目标”的**最后面**加上` --disable-features=msUndersideButton`。<br>
注意，`--`前面有个空格

把`系统盘:\Users\用户名\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar`里面的Edge快捷方式按同理修改

右键开始菜单里面的Edge，选择`打开文件位置`，对里面的Edge快捷方式同理修改