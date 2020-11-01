# 安装JDK

### 前言

如果你想要开发和运行一个 Java 程序，就必须要安装 JDK．所以，我们要做的第一件事就是安装JDK.

### 下载JDK

建议从 [Oracle 官网](https://www.oracle.com/java/technologies/javase-downloads.html)下载最新版本的 JDK，下面以下载 JDK15 的 Windows x64 版本为例：

![](https://netdisc.jianrry.com/images/java-se-download-1.png)

![](https://netdisc.jianrry.com/images/java-se-download-2.png)

![](https://netdisc.jianrry.com/images/java-se-download-3.png)

### 安装JDK

双击打开下载的文件，按照安装提示，一步步进行操作

![](https://netdisc.jianrry.com/images/java-se-install-1.png)

这一步你可以更改 JDK 的安装目录，将 JDK 安装到指定的目录下．或者保持默认，直接点击＂下一步＂．

![](https://netdisc.jianrry.com/images/java-se-install-2.png)

这一步，我将 JDK 安装到了 `C:\development\Java\jdk-15.0.1` 下

![](https://netdisc.jianrry.com/images/java-se-install-3.png)

![](https://netdisc.jianrry.com/images/java-se-install-4.png)

![](https://netdisc.jianrry.com/images/java-se-install-5.png)

### 设置环境变量

打开＂控制面板－系统和安全－系统＂，之后打开＂高级系统设置－高级－环境变量＂，最后打开＂系统变量＂

增加一条环境变量，变量名为`JAVA_HOME`，变量值为 JDK 的安装目录：

`C:\development\Java\jdk-15.0.1`

![](https://netdisc.jianrry.com/images/java-se-set-env-1.png)

编辑`Path`环境变量，新增一条属性：

`%JAVA_HOME%\bin`

![](https://netdisc.jianrry.com/images/java-se-set-env-2.png)

### 验证是否安装成功

打开 Windows PowerShell，输入`java -version`．JDK 安装成功后，会出现下面的提示：

![](https://netdisc.jianrry.com/images/java-se-set-env-3.png)

### 参考资料

[Java教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1252599548343744)

