java program control structure

# java程序控制结构
程序内部执行的顺序
1.	顺序控制
2.	分支控制
3.	循环控制
## 顺序控制
程序从上到下逐行地执行，中间没有任何判断和跳转

## 分支控制
让程序有选择的执行
### 单分支
```java
if(条件表达式）{
	执行代码块（如果只有一条语句可以不加{}）
}
```
### 双分支

```java
if(条件表达式）{
	执行代码块1
}else{
	执行代码块2
}
```
> else与最邻近的if构成一组
### 多分支

```java
if(条件表达式）{
	执行代码块1
}else if(条件表达式）{
	执行代码块2
}else if(条件表达式）{
	执行代码块3
}
...
}else{
	（不一定要用else作为最后的分支，else if也可以做最后的分支）
	执行代码块n
}
```
### 嵌套分支
在一个完整的分支结构中再嵌套了另一个完整的分支结构

```java
if(条件表达式）{

	if（条件表达式）{
		执行程序块
	}else{
		执行程序块
	}
	
}else{
	...
}

```
### swich分支结构

```java
switch(表达式){

	case 常量1:
	语句1;
	break;
	
	case 常量2:
	语句2;
	break;
	
	...
	
	case 常量n:
	语句n;
	break;
	
	default:
	default语句;
	break;
}
```
>流程图
![在这里插入图片描述](https://img-blog.csdnimg.cn/d282d343d0c3430aa6e858833581b22f.jpeg#pic_center)
>switch中的表达式返回值必须是：byte、short、int、char、enum、String
## 循环控制
### for循环控制
```java
for(循环变量初始化;循环条件;循环变量迭代){
	执行代码块
}
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/94da6bf6d32e4e109c7b4317560ebf3d.jpeg#pic_center)
> 1.	for语句内部定义一个变量，这个变量就不能在循环体之外使用，如果要使用该变量，就要确保在外部声明
> 2.	可以在各自独立的不同for循环中定义同名的变量
### while循环控制
```java
while(循环条件){
	执行代码块;
	循环变量迭代；
}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/2832a982cee14102a019de804e8366b9.jpeg#pic_center)
### do...while 循环控制
```java
循环变量初始化
do{
	执行代码块;
	循环变量迭代;
}while(循环条件);
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/36bc834d82e54dc18caa2a0aaf84b628.jpeg#pic_center)
### 多重循环控制
将一个循环体放在另一个循环体内，就形成了嵌套循环。
#### 九九乘法表
```java
public class NinenineMultiplicationTable{
//打印九九乘法表
	public static void main(String[] args){

		int i = 1;
		int j = 1;

		for(i = 1;i <= 9;i++){
			for(j = 1;j <= i;j++){
				System.out.print("\t" + j + "*" + i + "=" + i*j);
			}
			System.out.println('\n');

		}
	}
}
```
#### 空心金字塔

```java
public class HollowPyramid{
//打印空心金字塔
	public static void main(String[] args){

		int totalLevel = 10;
		//层数

		for(int i = 1;i <= totalLevel;i ++){

			//输出*之前，输出对应空格 = 总层数-当前层
			for(int k = 1;k <= totalLevel - i;k++){

				System.out.print(" ");

			}

			//控制打印每层*个数
			for(int j = 1;j <= 2 * i - 1;j++){

				if (j == 1||j == 2 * i - 1||i == totalLevel){
					System.out.print("*");
				}else{
					System.out.print(" ");
				}

			}

			//打印完一层自动换行
			System.out.println("");


		}

	}
}
```

## 跳转控制语句
### break
跳出最近的循环体，可以和标签搭配，跳出多重循环。
```java
label1:{ ....
label2:		{ ....
label3:			{ ....
				  break;
				  ....
				}
			}
		}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/9fc36a874efb4ecba127aa37e4da6746.jpeg#pic_center)

### continue
结束本次循环，继续执行下一次循环
```java
{ ...
	continue;
  ...
}
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/47e690139efa4a26bd441cbf857546d5.jpeg#pic_center)

### return 
使用在方法中，表示跳出所在的方法。