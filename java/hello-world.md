# 第一个 Java 程序

### 前言

在现实生活中，我们大家基本上都是用IDE（Eclipse, IntelliJ IDEA等）进行开发，基本上没有用到命令行．但使用命令行编译和运行 Java 源代码作为最基本的一项技能，还是需要我们掌握的．

### 步骤

1.打开文本编辑器，输入下面的代码，另存为`HelloWorld.java`

```text
public class HelloWorld {

        public static void main(String[] args){

            System.out.println("Hello World!");

        }

    }
```

2.在`HelloWorld.java`的存放目录下，打开Windows PowerShell，输入下面的代码

```text
javac HelloWorld.java
```

会在当前目录下，生成`HelloWorld.class`文件．

继续输入下面的代码

```text
java HelloWorld
```

会在Windows PowerShell的屏幕上，打印输出`Hello World!`

其实，输入`Java HelloWorld.java`，会达到同样的效果．

这是 Java 11 新增的功能，可以直接运行一个 Java 源代码文件．

在实际项目中，单个不依赖第三方库的Java源码是非常罕见的，所以，绝大多数情况下，我们无法直接运行一个Java源码文件，原因是它需要依赖其他的库。

![](https://netdisc.jianrry.com/images/hello-world.png)

### 解释

```text
public class HelloWorld {

}
```

`public` 表示这个类是公开的，`class` 表示 这是一个类，`HelloWorld`是这个类的名称（按照习惯，类的首字母必须大写），第一个`{}`花括号是这个类的定义，这一切构成了一个完整的类．

当我们将代码保存为文件时，文件名必须与类名一致．

```text
public static void main(String[] args){
        ...
}
```

`public`表示这个方法是公开的，`static`表示这是一个静态方法，`void`是这个类的返回类型（`void`表示这个类的返回类型是空），`main`是这个方法的名称，`String[] args`表明这个类的参数类型是`String[]`，第二个`{}`花括号是这个方法的定义，这一切构成了一个完整的方法．

上面定义的`main`方法（主方法）是一种固定的写法，是程序的入口，Java 程序总是从 `main` 方法开始执行的．

```text
System.out.println("Hello World!");
```

方法中的每一行代码都是以`;`结尾，这一行代码用于打印某个字符到屏幕上．

```text
javac HelloWorld.java
```

`javac` 是 Java 的编译器，会将`.java`结尾的 Java 源文件编译成 `.class`结尾的字节码文件．这一行代码将`HelloWorld.java`编译成`HelloWorld.class`，会在当前目录生成一个`HelloWorld.class`文件．

```text
java HelloWorld
```

`java` 是 Java 的虚拟机，会将`.class`结尾的字节码文件转换为对应平台的机器码，在物理计算机上运行．这一行代码将`HelloWorld.class`转换为机器码，所以屏幕上会打印输出的结果．

### 总结

一个 Java 源代码只能有一个 `public` 公共类．

类名首字母必须大写．

Java 源代码的文件名必须与类名一致．

Java 是一门介于编译型和解释型的编程语言，通过 JDK 中的 Java 编译器，将 Java 源代码（.java后缀名的文件）编译成 Java 字节码（.class后缀名的文件）．然后通过各个平台（Windows/Linux/MacOS）的 JVM ，将 Java 字节码（.class后缀名的文件） 转换为对应平台的机器码，在对应平台上运行．从而实现了＂一次编译，到处运行＂，所以说 Java 语言是跨平台的.

### 参考资料

[Java教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1252599548343744)

