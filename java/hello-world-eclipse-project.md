# Eclipse 创建一个 Java Project

### 前言

Eclipse 作为一款 IDE（集成开发环境），功能强大（支持各种插件），完全可以满足日常开发的需要．同时它免费提供给所有人下载使用，所以我推荐大家使用．

### 下载

建议在[官网](https://www.eclipse.org/downloads/packages/)下载，下载的版本是Eclipse IDE for Java Developers

![](https://netdisc.jianrry.com/images/eclipse-download-1.png)

如果下载速度慢，可以点击`Select Another Mirror`，重新选择一个镜像源．

![](https://netdisc.jianrry.com/images/eclipse-download-2.png)

如果几秒钟之后，还没有开始下载，点击`click here`重新下载．

![](https://netdisc.jianrry.com/images/eclipse-download-3.png)

### 安装

将下载后的文件，解压到指定的目录下，并创建桌面快捷方式即可

![](https://netdisc.jianrry.com/images/eclipse-install.png)

### 设置

#### 设置workspace

首次启动时，会弹出一个对话框，提示你设置workspace目录.

点击`Browser`，选择workspace目录，点击`选择文件夹`．

勾选上`Use this as the default and do not ask again`，下次启动就不会弹出提示了．最后点击`Launch`，启动Eclipse.

![](https://netdisc.jianrry.com/images/eclipse-setting-workspace-dir.png)

#### 设置文件编码

选择菜单`Windows－Preferences`，打开配置对话框．

依次打开`General-Workspace`，将`Text file encoding－Other`的选项设置为`UTF-8`，让所有文本都使用`UTF-8`编码．

将`New text file line delimiter－Other`的选项设置为`Unix`，即换行符使用 Unix 换行符`\n`，而不是 Windows 换行符 `\r\n`．

最后点击下方的`Apply and Close`，使修改生效．

![](https://netdisc.jianrry.com/images/eclipse-setting-file-encoding.png)

#### 调整字体大小

同上，依次打开`General－Appearance－Colors and Fonts－Basic－Text Font`，点击右侧的`Edit`，打开字体对话框．修改完成之后，点击下方的`Apply and Close`，让修改生效．

![](https://netdisc.jianrry.com/images/eclipse-setting-text-font.png)

#### 显示行号

同上，依次打开`General－Editors－Text Editors`，勾选`Show line number`.最后点击下方的`Apply and Close`，使修改生效．

![](https://netdisc.jianrry.com/images/eclipse-setting-line-number.png)

#### 设置JRE

同上，依次打开`Java－Installed JREs`，将已经安装的JRE编辑为 JDK15，与 JDK 的版本保持一致．

最后点击下方的`Apply and Close`，使修改生效．

如果还有其他版本的 JDK ，建议删除．

![](https://netdisc.jianrry.com/images/eclipse-setting-installed-jres.png)

#### 设置编译器

同上，依次打开`Java－Compiler`，将`Compiler compliance level`调整为15，与 JDK 的版本保持一致．

不要勾选`Use default compliance settings`，勾选上`Enable preview features for Java 15`，使用 JDK 15 的全部特性．

最后点击下方的`Apply and Close`，使修改生效．

如果 `Compiler compliance level`没有出现15的选项，请更新Eclipse到最新版，然后重启．如果更新后，还没有出现15的选项，请打开`Help－Eclipsemarkplace`，搜索`Java 15 Support`插件进行安装，重新启动即可．

![](https://netdisc.jianrry.com/images/eclipse-setting-java-compiler.png)

### Eclipse 区域

![](https://netdisc.jianrry.com/images/eclipse-ide.png)

1是编辑器，用于输入代码．

2是 Java 项目的视图

3是输出信息的视图

4是当前编辑的源代码的结构视图

5用于切换不同的视图

### 新建 Java Project

在 Eclipse 菜单选择`File-New-Java Project`

![](https://netdisc.jianrry.com/images/eclipse-java-project-1.png)

输入项目名，点击`Next`

![](https://netdisc.jianrry.com/images/eclipse-java-project-2.png)

不要勾选`Create module-info.java file`，因为模块化机制在后面会讲到．

最后点击`Finish`，一个 Java Project 就创建完成了．

![](https://netdisc.jianrry.com/images/eclipse-java-project-3.png)

展开`HelloWorld`项目，选择`src`源码目录，右键选择`New Java Class`．输入类名，最后点击`Finish`，就创建了一个类．

![](https://netdisc.jianrry.com/images/eclipse-java-project-4.png)

打开`HelloWorld`类，写入下面的代码，然后保存．

选择`HelloWorld`类，右键选择`Run As－Java Application`，运行这个类．

![](https://netdisc.jianrry.com/images/eclipse-java-project-5.png)

在下方的`Console`窗口就可以看到运行的结果了．

如果没有出现`Console`窗口，打开`Window－Show View－Console`，就会出现`Console`窗口了．

![](https://netdisc.jianrry.com/images/eclipse-java-project-6.png)

### 参考资料

[Java教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1252599548343744)

