这个项目是为了方便在Unity开发移动端时需要上传头像，上传反馈图片之类的效果而开发的。

为了显示效果近似，用到了网上某大神写的仿IOS ActionSheet稍加改动。

这里为Android平台源码，插件和另一部分源码在另一个工程。
[传送门]:http://git.oschina.net/lovewestwind/unityphotoplugins

另一个工程里有demo项目和plugins源码和IOS源码，在Assets/Plugins/IOS/目录下。

IOS部分截图

![IMG_2745](doc/IMG_2746.PNG)

![IMG_2745](doc/IMG_2745.PNG)

Android部分截图

![android1](doc/android1.jpg)

![android2](doc/android2.png)

![android3](doc/android3.png)

NextVersion:

1. IOS平台弹出ActionSheet会黑屏，具体原因是跳到了IOS的Controller，不这样的话会导致nil。
2. IOS目前是用Base64编码通过Unity的SendMessage回传的，目前写的固定宽高，下一步会以分隔符传输图片尺寸信息，然后加上encode的图片数据回传。
3. Android方面可以直接回传拍照和所选照片的路径，在权限包括路径问题上还亟待解决。

