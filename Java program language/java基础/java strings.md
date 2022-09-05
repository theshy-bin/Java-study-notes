# java字符串概念
>java字符串就是Unicode字符序列。
java没有内置的字符串类型，而是在标准java类库中提供了一个预定类，很自然地叫做String
每个用双引号括起来的字符串都是String类的一个实例

```java
String greeting = "hello";
String s = "";
```
## 子串
String类的substring方法可以从一个较大的字符串提取一个子串。
```java
String greeting = "hello";
String s = greeting.substring(0,3);
```
>复制位置0到2的字符

## 字符串拼接
java语言允许使用+号连接两个字符串
当将一个字符串和另一个非字符串的值进行拼接时，后者会被转换成字符串，这种特性常用于输出语句中
```java
System.out.println("1+2="+sum);
```
### 基本数据类型转String类型
基本类型的值+""
```java
int n = 100;
String ns = n + "";
//ns = "100"
```

### String类型转基本数据类型
通过基本类型的包装类调用parseXX方法
```java
int n = Integer.parseInt("123");
//n = 123;
```
>要确保String类型能够转成有效的数据，如果格式不正确，就会抛出异常，程序终止

## 字符串比较
Java中的字符串存放在公共的存储池中。字符串变量指向存储池中相应的位置。如果复制一个字符串变量，原始字符串与复制的字符串共享相同的字符

可以使用equals方法检查两个字符串是否相等
```java
greeting.equals(t)
```
>一定不要用==检查是否相等，这个运算符只能够确定两个字符串是否放置再同一位置上
## 空串与null串
空串""是长度为0和内容为空的字符串。
String变量还可以存放一个特殊值，名为null，这表示目前没有任何对象与该变量关联。
```java
if(str != null && str.length() != 0)
//检查一个字符串既不是null也不是空串
```

## 码点与代码单元
java字符串由char值序列组成。一个char值对应一个码点，一个码点一般对应一个代码单元，辅助字符需要一对代码单元表示
length方法将返回采用UTF-16编码表示的给定字符串所需的代码单元数量
```java
String greeting = "hello";
int n = greeting.length();
//n = 5
```
s.charAt(n)将返回位置n的代码单元，n介于0~s.length()-1之间
```java
char first = greeting.charAt(0);
//first = 'h'
```
