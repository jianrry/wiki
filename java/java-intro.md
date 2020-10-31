# Java 简介

### 简介

Java 是一门编程语言，由 Sun 公司中的 詹姆斯·高斯林 和同事们共同研发，在 1995 年正式推出。

后来 Sun 公司被 Oracle （甲骨文）公司收购，Java 成为了 Oracle 公司的产品。

### 版本

随着 Java 的发展，Java 分为３个版本：

* Java SE：Standard Edition（Java 标准版，包含了标准的 JVM 和标准库）
* Java EE：Enterprise Edition（Java 企业版，在 Java SE 的基础上增加了大量的 API 和库）
* Java ME：Micro Edition（Java 微型版，针对嵌入式设备的＂阉割版＂）

它们之间的关系是：

┌───────────────────────────┐ │Java EE │ │ ┌────────────────────┐ │ │ │Java SE │ │ │ │ ┌─────────────┐ │ │ │ │ │ Java ME │ │ │ │ │ └─────────────┘ │ │ │ └────────────────────┘ │ └───────────────────────────┘

### 时间线

从1995年发布1.0版本开始，到目前为止，最新的Java版本是Java 15：

| 时间 | 版本 |
| :--- | :--- |
| 1995 | 1.0 |
| 1998 | 1.2 |
| 2000 | 1.3 |
| 2002 | 1.4 |
| 2004 | 1.5 / 5.0 |
| 2005 | 1.6 / 6.0 |
| 2011 | 1.7 / 7.0 |
| 2014 | 1.8 / 8.0 |
| 2017/9 | 1.9 / 9.0 |
| 2018/3 | 10 |
| 2018/9 | 11 |
| 2019/3 | 12 |
| 2019/9 | 13 |
| 2020/3 | 14 |
| 2020/9 | 15 |

### 名词解释

#### JVM

JVM 是 Java Virtual Machine（Java 虚拟机）的缩写，可以看成是一台虚拟的计算机，将 Java 字节码（.class后缀名的文件） 转换为机器码，在物理计算机上运行．

Java 是一门介于编译型和解释型的编程语言，通过 JDK 中的 Java 编译器，将 Java 源代码（.java后缀名的文件）编译成 Java 字节码（.class后缀名的文件）．然后通过各个平台（Windows/Linux/MacOS）的 JVM ，将 Java 字节码（.class后缀名的文件） 转换为对应平台的机器码，在对应平台上运行．从而实现了＂一次编译，到处运行＂，所以说 Java 语言是跨平台的.

#### JRE 与 JDK

JRE 是 Java Runtime Environment（Java 运行时环境）的缩写，包含了 JVM 和运行 Java 程序的其他环境支持．如果你想要运行一个 Java 程序，只需要安装 JRE 就可以了，无需安装 JDK.

JDK 是 Java Development Kit（Java 开发工具包），包含了 JRE 和编译器 调试器等．如果你想要开发一个 Java 程序，就必须安装 JDK．安装 JDK 之后，就包含了 JRE，也可以运行 Java 程序.

它们之间的关系是

┌─ ┌──────────────────────────────────┐ │ │ Compiler, debugger, etc. │ │ └──────────────────────────────────┘ JDK ┌─ ┌──────────────────────────────────┐ │ │ │ │ │ JRE │ JVM + Runtime Library │ │ │ │ │ └─ └─ └──────────────────────────────────┘ ┌───────┐┌───────┐┌───────┐┌───────┐ │Windows││ Linux ││ macOS ││others │ └───────┘└───────┘└───────┘└───────┘

#### Oracle JDK 与 OpenJDK

Oracle JDK 是 Java 的商业版本，由 Oracle 公司完全开发．

OpenJDK 是 Java 的开源版本，基于 Sun 公司捐赠的一部分 Java 源代码（里面剔除了商业功能的代码），由 Oracle 和社区共同开发．

Oracle JDK 与 OpenJDK 之间的具体区别，可以参考下面的这篇文章：

[Java官方（Oracle/Sun）发布的JDK，和开源项目OpenJDK，里面包含的JVM是否相同？ - RednaxelaFX的回答 - 知乎](https://www.zhihu.com/question/19882320/answer/36068407)

### 参考资料

[Java教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1252599548343744)

