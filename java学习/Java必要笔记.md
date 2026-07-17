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
