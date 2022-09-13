java variable

# 变量与常量
>**变量**表示内存中的一个存储区域，java是一种强数据类型语言，每一个变量都要声明一种类型。
![在这里插入图片描述](https://img-blog.csdnimg.cn/dfb397090fc74338a7e79c4c6260a6a2.jpeg#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/9435a5a6b6cf4acfbbb00691ac6f1a75.jpeg#pic_center)


>**常量**就是现实中的要处理的数据
# java数据类型概括
![在这里插入图片描述](https://img-blog.csdnimg.cn/face9f1e03bb442e83ede9909a413d0a.jpeg#pic_center)
## 整型
1.	长整型数值有后缀L或l
2.	十六进制有前缀0x或0X
3.	八进制有前缀0
4.	二进制有前缀0b或0B
## 浮点型
1.	float类型数值有后缀F或f
## 字符型
1.	char的本质是一个整数，在输出时，是unicode码对应的字符（汉字和字母统一都是占两个字符）
2.	char类型的值可以表示为十六进制值，其范围从\u0000到\uffff
## 布尔类型
1.	boolean类型数据只允许取值true或false

## 引用数据类型
**值传递，但存储内容为地址，即值为地址**
# 自动数据类型转换
>**运算时**精度小的类型自动转换为精度大的数据类型
>byte，short，char在计算时首先转换为int类型
>当把精度大的数据类型**赋值**给精度小的的数据类型时，就会报错，反之就会进行自动转换
![在这里插入图片描述](https://img-blog.csdnimg.cn/e905d427cace4fa6a3f922c3c7d6b8bd.jpeg#pic_center)
# 强制数据类型转换
>**赋值时**将容量大的数据类型转换为容量小的数据类型。使用时要加上强制转换符()。
>char类型可以保存int的常量值，但不保存int的变量值
>byte，short，char在计算时首先转换为int类型
