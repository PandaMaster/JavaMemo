# JavaMemo

Java学习整理

## 数据类型

8种基本类型

| 类型      | size(byte) | 取值范围                |
| --------- | ---------- | ----------------------- |
| int       | 4          | -2147483648～2147483647 |
| short     | 2          | -32768～32767           |
| long      | 8          | -9223372036854775808～9223372036854775807 |
| byte      | 1          | -128～127               |
| float     | 4          | 有效位数为6-7位         |
| double    | 8          | 有效位数为15位          |
| boolean   | 1          | true/false              |
java中没有unsigned类型

## 数值类型转换

虚线表示转换时有精度丢失

## 多重选择--switch
```c
switch (select) {
case value1:
case value2:
    statement;
    break;
case value3:
    statement;
    break;
case value4:
    statement;
    break;
default:
    statement;
}
```
case标签必须是整数(int、char)或者枚举常量  
case语句后面如果没有break，会执行后面的case分支

## static关键字
在没有创建任何对象的前提下，仅仅通过类本身来调用static方法/变量。  
在static方法内部不能调用非静态方法,但是非静态方法可以调用static方法。  
static代码块可以用来优化程序性能，因为它只会在类加载的时候执行一次。  
```java
class Person{
    private Date birthDate;
    private static Date startDate;
    private static Date endDate;
    static{
        startDate = Date.valueOf("1958");
        endDate = Date.valueOf("1985");
    }
     
    public Person(Date birthDate) {
        this.birthDate = birthDate;
    }
     
    boolean isBornBoomer() {
        return birthDate.compareTo(startDate) >= 0 && birthDate.compareTo(endDate) < 0;
    }
}
```
<font color=red>static不允许用来修饰局部变量</font>

## 数组
数组声明`int[] a;`  
静态初始化  
`String[] a = new String[] {"One", "Two, "Three"};` `String[] a = {"One", "Two, "Three"};`  
动态初始化  
```c
int[] bookNum = new int[5];
bookNum[0] = 50;
... ...
```
数组变量存放在栈内存中，数组变量只是一个引用变量，指向实际的数组对象。  
数组对象存放在堆内存中，初始化完成后，数组对象所占空间将不可改变。如果数组对象失去引用，就变为垃圾，等待回收。
