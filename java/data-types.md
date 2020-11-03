# Java 数据类型

### 前言

变量通过申请内存来存储值，当创建变量的时候，需要在内存中申请空间。

内存管理系统根据变量的类型为变量分配存储空间，分配的空间只能用来储存该类型数据。

因此，通过定义不同类型的变量，可以在内存中储存整数、小数或者字符。

### 基本类型

Java 中有 8 种基本数据类型，分为三大类：

* 数值型：
  * 整型：byte、short、int、long
  * 浮点型：float、double
* 字符型：char
* 布尔型：boolean

boolean 只有两个值：true、false，可以使用 1 bit 来存储，但是具体大小没有明确规定。

JVM 会在编译时期将 boolean 类型的数据转换为 int，使用 1 来表示 true，0 表示 false。

JVM 支持 boolean 数组，但是是通过读写 byte 数组来实现的。

| 基本数据类型 | 默认值 | 字节 | 位数 | 包装类 |
| :--- | :--- | :--- | :--- | :--- |
| byte | 0 | 1 | 8 | Byte |
| short | 0 | 2 | 16 | Short |
| int | 0 | 4 | 32 | Integer |
| long | 0L | 8 | 64 | Long |
| float | 0.0f | 4 | 32 | Float |
| double | 0.0d | 8 | 64 | Double |
| char | 'u0000' | 2 | 16 | Character |
| boolean | false |  |  | Boolean |

### 引用类型

除了上面的基本类型，其他的全部是引用类型，最常见的是 String 字符串．

对象、数组都是引用数据类型。

所有引用类型的默认值都是null。

### 装箱和拆箱

* 装箱：将基本类型用它们对应的引用类型包装起来；
* 拆箱：将包装类型转换为基本数据类型；

以 Integer 为例，装箱的时候自动调用的是Integer的valueOf\(int\)方法。而在拆箱的时候自动调用的是Integer的intValue方法

下面这段代码是Integer的valueOf方法的具体实现：

```text
public static Integer valueOf(int i) {
        if(i >= -128 && i <= IntegerCache.high)
            return IntegerCache.cache[i + 128];
        else
            return new Integer(i);
    }
```

而其中IntegerCache类的实现为：

```text
 private static class IntegerCache {
        static final int high;
        static final Integer cache[];

        static {
            final int low = -128;

            // high value may be configured by property
            int h = 127;
            if (integerCacheHighPropValue != null) {
                // Use Long.decode here to avoid invoking methods that
                // require Integer's autoboxing cache to be initialized
                int i = Long.decode(integerCacheHighPropValue).intValue();
                i = Math.max(i, 127);
                // Maximum array size is Integer.MAX_VALUE
                h = Math.min(i, Integer.MAX_VALUE - -low);
            }
            high = h;

            cache = new Integer[(high - low) + 1];
            int j = low;
            for(int k = 0; k < cache.length; k++)
                cache[k] = new Integer(j++);
        }

        private IntegerCache() {}
    }
```

从这2段代码可以看出，在通过valueOf方法创建Integer对象的时候，如果数值在\[-128,127\]之间，便返回指向IntegerCache.cache中已经存在的对象的引用；否则创建一个新的Integer对象。

注意：

Integer、Short、Byte、Character、Long这几个类的valueOf方法的实现是类似的。

Double、Float的valueOf方法的实现是类似的。

Double类的valueOf方法不同于Integer，是因为在某个范围内的整型数值的个数是有限的，而浮点数却不是。

### 参考资料：

[Java教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1252599548343744)

[深入剖析Java中的装箱和拆箱 - Matrix海子 - 博客园](https://www.cnblogs.com/dolphin0520/p/3780005.html)

