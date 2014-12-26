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

