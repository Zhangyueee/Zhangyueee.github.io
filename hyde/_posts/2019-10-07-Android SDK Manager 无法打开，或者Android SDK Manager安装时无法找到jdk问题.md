# Android SDK Manager 无法打开，或者Android SDK Manager安装时无法找到jdk问题

## 情况：

在有段时间不去使用Android SDK Manager后，你有可能会发现自己的Android SDK Manager打开时闪一下黑框就不见了，无法正常运行。不管怎么覆盖安装，调整环境变量都无法解决，这时大概率原因在于你的Java jdk版本变动了，Java 10版本并不支持Android SDK Manager。包括有时使用Android SDK Manager的安装包发现无法找到jdk，分明环境变量确保是对的，依旧检索不到，这时大概率也是这个问题

![](https://raw.githubusercontent.com/Zhangyueee/Storage/master/Android SDK Manager 无法打开，或者Android SDK Manager安装时无法找到jdk问题.jpg)

## 解决：

环境变量改回Java8版本，但是这时，去oracle官网上下载Java8版本你会发现需要登陆了。这里分享账户密码，仅供学习使用。

账号:2696671285@qq.com

密码:Oracle123

账号密码转自：https://blog.csdn.net/LinBilin_/article/details/50217541