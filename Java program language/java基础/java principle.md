# java特点
1.	面向对象(oop)
2.	健壮的
3.	跨平台性的(JVM)
4.	解释性：解释性语言，编译后的代码，不能直接被机器执行，需要解释器来执行；编译性语言，编译后的代码，可以直接被机器执行，c/c++。
# java应用程序的运行机制
![在这里插入图片描述](https://img-blog.csdnimg.cn/f4febe07d96d4f3dbc13d4d3e6557376.jpeg#pic_center)
# java程序基本组成

```java
public class Hello {
	//定义一个公有的类Hello，一个文件必须有且只有一个公有类(public)
	public static void main(String[] args){
		//定义一个main方法，程序的入口

		System.out.println("yyf is studying java");
	}//方法体或方法块
}//类体或类块

class dog {
	public static void main(String[] args){

		System.out.println("yyf hava a dog");
	}
	
}

class lion{
	public static void main(String[] args){

		System.out.println("yyf have not a lion");
	}

}
```
> java源文件的基本组成部分是类（class)
> 一个源文件最多只能有一个public类，其他类的个数不限
> Java应用程序的执行入口是main()方法
# Java转义字符
第一个斜杠“\"表示转义，将一个字符转换成另一字符

```java
public class ChangeChar{
//转义字符
	public static void main(String[] args){

		System.out.println("姓名\t性别\t年龄");
		//\t 一个制表位

		System.out.println("如果冬天来了，\n春天还会远吗？");
		//\? 一个换行符

		System.out.println("\\");
		//\\ 一个\

		System.out.println("\"");
		//\" 一个"

		System.out.println("\'");
		//\' 一个'

		System.out.println("夏春秋冬\r春夏");
		//\r 一个回车符，光标移动到当先行的最左侧
	}
}
```
# java注释
1.	单行注释 //
2.	多行注释/* */
3.	文档注释
> 文档注释可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档，一般写在类

```java
/**
 * @author yyf
 * @version 1.0
 */
public class DocumentationNotes{

	public static void main(String[] args){

			int n1 = 1 + 2;
			int n2 = 5 + 10;
			int sum = n1 + n2;

			System.out.println(sum);

	}
}
```
javadoc -d 文件夹名 -author -version -DocumentationNotes.java
![生成的注释文件](https://img-blog.csdnimg.cn/c44c4b2bcdb045d29c9a74f2fce5cbb5.png#pic_center)
