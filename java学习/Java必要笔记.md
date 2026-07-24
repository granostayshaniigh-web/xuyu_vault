# 第一章
1. 计算机语言：
2. class：创建一个类，定义一个类。后面是类名。类的范围后面的大括号包含的
```java
//package:表示当前的类(HelloWorld)定义在那个包(practice.test)下面
package practice.test;  
//Class 是定义一个类,类是java项目中最基本的组成单元
public class HelloWorld {   
//public static void main,这是程序的主入口,会从主入口开始逐行往下执行
    public static void main(String[] args) {  
        System.out.println("Hello World");  
    }  
}
```
3. 程序中的数据，Java 中字面量分为：整数、小数、字符串、字符、布尔，空。
4. 变量是存储数据的，里面的数可以变。变量是指那个放数据的那个框
5. 经常发生改变的数据可以用变量来存储
6. 一个自己也就是1B等于八个比特位，int占四个字节也就是32个比特位
7. long类型的变量在定义的时候数字后面加一个L ，float后面要加一个F 。
8. 字符类型char定义的时候需要用单引号。单引号里面的字符只能是一个
9. 标识符只能是由数字，字母，下划线，以及符号，符号只能是$。
10. 小数参与计算可能不精确
```java
package practice.test;

import java.util.Scanner;

public class a_little_example {
    public static void main (String[] args){
        double a;
        double b;
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the first number a");
        a=sc.nextDouble();
        System.out.println("Enter the second number b");
        b=sc.nextDouble();
        System.out.println(a+b);
        System.out.println(a-b);
        System.out.println(a*b);
        System.out.println(a/b);
        System.out.println(a%b);
    }
}

D:\idea\bin\java.exe "-javaagent:D:\idea\IDEA_program\IntelliJ IDEA 2025.1\lib\idea_rt.jar=63304" -Dfile.encoding=UTF-8 -Dsun.stdout.encoding=UTF-8 -Dsun.stderr.encoding=UTF-8 -classpath D:\idea\IDEA_program\java_program\out\production\java_program practice.test.a_little_example
Enter the first number a
1.1
Enter the second number b
1.01
2.1100000000000003
0.09000000000000008
1.1110000000000002
1.0891089108910892
0.09000000000000008

进程已结束，退出代码为 0
```
11. 数字运算：类型不一样不能运算，需要转成同类型才能计算
	- 隐式转换，小范围转成大范围，不需要写代码。例外：如果有byte、short类型的数据，计算时要转为int
	- 强制转换，大范围转成小范围，需要写代码，会导致精度丢失。int a；byte b=（byte）a；
12. 字符串拼接与数字拆分。
```java
package practice.test;  
import java.util.Scanner;  
public class num_divide {  
    public static void main (String[] args){  
        System.out.println("enter the number");  
        Scanner sc = new Scanner(System.in);  
        int seconds =sc.nextInt(); 
        //数字拆分 
        int hours=seconds/3600;  
        int minutes=seconds%3600/60;  
        int second=seconds%3600%60;
        //字符串拼接  
        System.out.println("小时:"+hours);  
        System.out.println("分钟:"+minutes);  
        System.out.println("秒:"+second);  
    }  
}
```
13. 逻辑运算符：逻辑与&、逻辑或|、逻辑非！、短路与&&、短路或||
14. 三元运算符
15. 运算符的优先级，小括号的优先级高于所有。
# 第二章
13. switch语句中小括号中的语句得到的是一个确定的值==（这个值可以是字符，整数不能是小数和长整数，枚举，字符串）==。这个确定值与case后面的值（==不能用变量表示，不能重复==）进行匹配，匹配上了就执行后面的语句。==并且default和case没有先后之分，也可以省略，所以没有和case匹配时，不会有输出。==case后面可以写==多个值==，用逗号隔开。->可以写在case后面,在大括号里面不用写break，但是冒号和->不能同时写。==yield程序最后的分号。==
# 第三章
13. 无限循环while（true）{}；for（；；）{}；do{}while（true）；其中true不能用1代替，java中int不能转化为bool
14. 生成随机数：
```java
Random r = new Random()
第一种写法：int n = r.nextInt();默认在int范围随机取值
第二种写法：int n = r.nextInt(n);默认在 0~n-1 范围随机取值
第三种写法：int n = r.nextInt(a,b);默认在 a~b-1 范围随机取值
```
# 第四章
15. 数组静态初始化：`int arr [] = new int [] {1,2,3};`
	数据类型  数组名 \[ ] = new 数据类型 \[ ] {数据值，数据值……}；
	简写：`