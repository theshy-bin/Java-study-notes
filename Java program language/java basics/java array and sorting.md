java array and sorting

# java数组
## 定义
数组是一种数据结构，也是一种数据类型，用来存储同一类型值的集合。通过一个整型下标可以访问数组中的每一个值。
```java
int[] a;
int a[];
//可以用两种形式声明变量a,一般用第一种风格，因为它将类型int[](整型数组）与变量名a分开了
int[] a = new int[100];
//声明并初创建了数组a
int[] a = {1,3,4,5,6,7,8,9,0};
//声明并初始化了数组a,数组下标从0开始
int length = a.length;
//获得数组中元素个数
```
## 数组拷贝与值拷贝
### 地址传递
在java中，允许一个数组变量拷贝给另一个数组变量。这时，两个变量引用同一个数组：
```java
int[] arr1 = {1,2,3};
int[] arr2 = arr1;
arr2[0] = 10;
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/28d9ea0b5dae4ab4bb51d7620fc85964.jpeg#pic_center)
### 值转递
```java
int[] arr1 = {1,2,3};
int[] arr2 = new int[arr1.length];
for(int i = 0;i < arr1.length;i++){
	arr2[i] = arr1[i];
}
```
### 数组反转
将数组的元素内容反转
```java
int[] arr2 = new int[arr1.length];
for(int i = arr1.length -1,j = 0;i >= 0;i -- ,j ++){
	arr2[j]=arr1[i];
}
arr1 = arr2;
//逆序赋值法
```
### 数组添加/扩容
实现动态的给数组添加元素效果，实现对数组扩容
```java
int[]arr = new int[arr1.length + 1];
for(int i = arr1.length -1,j = 0;i >= 0;i -- ,j ++){
	arr2[j]=arr1[i];
}
arr2[arr2.length - 1] = 4;
arr1 = arr2;
```
## 二维数组
### 定义
二维数组的本质就是一维数组，只不过形式上是二维的。
```java
int[][] arr = new int[2][3];
//声明并创建二维数组
arr[1][1] = 8;
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/80d83bdb71f4400dbb944f63c62a3864.jpeg#pic_center)
### 杨辉三角

```java
public class YangHuiTriangle{

	public static void main(String[] args){

			//使用二维数组打印一个10行杨辉三角
		int[][] YHT = new int[10][];

				for(int i = 0;i < YHT.length;i ++){

					YHT[i] = new int[i+1];
				
				//给每个一维数组开辟空间

					for(int j = 0;j < YHT[i].length;j ++){
						if(j == 0 || j == YHT[i].length - 1){
							YHT[i][j] = 1;
							//每一行第一个和最后一个元素都是1
						}else{
							YHT[i][j] = YHT[i-1][j] + YHT[i-1][j-1];
							//中间的元素
						}
					}
				
				}

		for(int i = 0;i < YHT.length;i++){
			for(int j = 0;j < YHT[i].length;j++){
				System.out.print(YHT[i][j]+"\t");
			}
			System.out.println();
		}
	}
}
```

# 排序
排序是将多个数据，依指定的顺序进行排列的过程
## 冒泡排序（Bubble sort)
```java
for(i = 0;i < arr.length-1;i++){
	//第一层for循环用于确定有arr.length-1个数需要确定位置
	int temp = 0;
	//用于交换数
	for(j = 0;j < arr.length-1-i;j++){
	//第二层for循环用于确定每次循环要比较几次
		if(arr[j] > arr[j+1]){
		temp = arr[j];
		arr[j] = arr[j+1];
		arr[j+1] = temp;
		//交换位置
		}
	}

}
```
## 选择排序 （selection sort)
```java
for(int i = 0;i < arr.lenth-1;i++){
	//确定arr.length-1个数的位置
	int subscript = i;
	//下标指向该循环最小值
		for(int j = i + 1 ;j < arr.length;j ++）{
			subscript = arr[j] <arr[subscript]?j:subcript;
		}
		//遍历一次找到最小值
		swap(arr,i,subcript);
	
}
```

## 插入排序（insertion sort)
```java
for(int i = 1;i < arr.lenth;i ++){
	//要插入几次数
	for(int j = i;j >= 0;j --){
	//当插入一次时需要循环几次
		if(arr[j - 1] > arr[j]){
			swap(arr,j,j-1);
		}else{
			break;
			//前一个数小则退出循环
		}
	}
}
```




