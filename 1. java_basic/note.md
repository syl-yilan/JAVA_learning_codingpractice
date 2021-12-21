[toc]
# JAVA基础导学
目标：后台管理系统、文件的读写
案例：猜数、学生/老师信息管理系统
# JAVA基础语法
## 环境搭建+入门
内容：跨平台、JRE JKD JVM、下载安装、DOS命令、环境变量、简单代码实现、NOTEPAD、注释、关键词
平台（操作系统：WIN\ MAC\ LINUX）
### 跨平台属性
JAVA程序可以在任意操作系统上运行
原理：在不同平台上安装一个与平台对应的JAVA虚拟机（**JVM**: JAVA VIRTUAL MACHINE）
![3b41a7636a7ab6d2b482030882837b3b.png](en-resource://database/589:1)
JVM本身不可以跨平台
### JAVA程序开发步骤
```mermaid
graph TD
A[编写] -->|javac| B(编译)
B[编译] -->|java| C(运行)
```

编写：

* **JRE**(JAVA RUNTIME ENVIRONMENT, 包含虚拟机和JAVA核心类库)
* 类：JAVA文件在代码中的几种体现（类=JAVA文件，一个Java文件，一个Java类）
* 类库：存放多个Java文件的仓库
* 核心类库：Java已经写好的，非常核心的代码仓库，存放在JRE中，在外面写代码时会被用到

编译：javac

* .java为源文件，无法被JVM所识别执行
* 翻译工具：**JDK**(JAVA DEVELOPMENT KIT)
* 编译成功会产生一个.class文件，这个文件可以被JVM识别执行

运行：JDK运行工具，运行在JVM中
![f68fc8deada78c48517e561658f0e623.png](en-resource://database/593:1)
![df50511c89ae94c8620a3dfdbf43971c.png](en-resource://database/592:1)
### JAVA发展史
![c674b8fdf3a54b4f42383b97f03fc256.png](en-resource://database/590:1)
### JAVA安装
![c89c5394164bd93a2ca54f1f4875a80b.png](en-resource://database/591:1)
WIN+R CMD 或
在目标文件夹的路径栏输入CMD

常用DOS命令
![1c8eff4c6392d6b6a1d0fdc5e88ea2d5.png](en-resource://database/588:1)
![515bb082ad82f38464159f008822fbf2.png](en-resource://database/596:1)
![683171ba1baf0ebd8f2f8afa2b05f450.png](en-resource://database/600:1)

### 环境变量的配置
配置原因：Java文件和Java程序安装的位置不同
方式：
![eacce628ae62f8ee5291ba1d05cc8b65.png](en-resource://database/602:1)
![265e06dda2e8700e807b49defd785899.png](en-resource://database/594:1)
![680515ed5d967147cee05e0f6ddd6b83.png](en-resource://database/599:1)
![f47adda8a8ca00ca308b57016dd6899f.png](en-resource://database/603:1)
![538672fe169a36a2187086a37681fa50.png](en-resource://database/597:1)
![ca59fb3c84394be9302d29fa1ac3a3e5.png](en-resource://database/601:1)
![3f3b5839afd5ccd104803eb649405641.png](en-resource://database/595:1)
### hello, world!
区分大小写
编译 JAVAC
运行
JAVA
![5b5b7fef6b633bbcb14e6f6d04b7c298.png](en-resource://database/598:1)
如果不加public的话，文件名好class名可以不一致；但如果加了public的话就得一致（不然会报错）。
### 注释
* 单行注释 //
* 多行注释 /*    */ 
* 文档注释 /**      */
### 关键词

1. 关键词字母全是小写
2. 代码编辑器里对关键词有特殊的颜色标记
*main不是关键词，但也非常关键，相当于程序的入口识别

## 数据类型及转换
内容：常量、变量、数据类型、键盘录入、标识符、类型转换
### 常量
代码执行过程中，值不会发生改变的量

* 字符串常量 双引号
* 整数常量
* 小数常量
* 字符常量 单引号（单个字符）
* 布尔常量 true or false
* 空常量 null
![90bb66ca1d903cc5bd092dee1e590ec1.png](en-resource://database/604:1)
### 变量
经常发生改变的值
![ac2ebd5ef3e66dd45758fa1eb56b4907.png](en-resource://database/606:1)
变量就是内存中的存储空间，空间中存储着经常发生改变的量（数据）
数据类型 变量名 = 数据值
### 基本数据类型
![db9cc4dc13d7be1fa06cff29c1e4a668.png](en-resource://database/608:1)
整数里常用int，小数里常用double
![9e7ec4e9dc60a65739cde9e86f9dfb5d.png](en-resource://database/605:1)
![d74e2625bdc1f2df4f7a5380db8eb1e2.png](en-resource://database/607:1)

*不能重复定义变量，比如说下面这样写，程序就会报错
`int a = 2; int a = 3;`
*分号作为一条语句的结束（最后一条语句也要加分号）
*一条语句可以多个赋值，例如：
`int a = 1, b = 2, c = 3;`
*变量必须初始化
*float和long类型定义时必须加标识
![2600ef3f45dd11273d41e3b6db62b4bf.png](en-resource://database/610:1)
*变量作用域：所在的大括号里
### 键盘录入
S1 导包 `import java.util.Scanner;`
S2 创建对象 `Scanner sc = new Scanner(System.in);`
S3 使用变量接受数据 `int a = sc.nextInt();`
![1e753430b42f64a555c65c99da52f2ad.png](en-resource://database/609:1)
### 标识符
自己起的名字
* 由数字、字母、下划线_、美元符$组成
* 不能由数字开头、不能是关键词、区分大小写
常见的命名约定：（小驼峰大驼峰）
![3368aea8d82fd05e181ad1bed57c4bf3.png](en-resource://database/611:1)
### 类型转换
![d47a58aa14725442cf277aa900d6fdb3.png](en-resource://database/612:1)
隐式转换（小精度——>高精度）
`int a = 10;
float b = a;`
强制转换（高精度——>小精度）（直接丢掉小数部分，不进行四舍五入的转换）
`int a = 10;
byte b = (byte)a;`
![a9062c51c1e19653f6d42b1a69c20521.png](en-resource://database/619:1)
![b4c03120d0fc13a4b056ba103dd4b136.png](en-resource://database/621:1)
**整数常量默认为int类型**
## 运算符
运算优先级：算术运算符>比较运算符>赋值运算符>逻辑运算符>三元运算符
### 算数运算符
运算符：对常量或变量进行操作的符号
表达式：用运算符把常量或变量连接起来符合语法的式子
![4b634e9941229f75c306bb3e666df425.png](en-resource://database/614:1)
int相除得到整数
如果要有小数的话得有float型参与运算
### 字符的运算
ASCII码表：字节-字符的对应关系
![b1ed967724053bca85061c30fcfe8099.png](en-resource://database/620:1)
码表不用全记，着重记忆：
![1d18fcf4d720dad2bf5a76413f8b2557.png](en-resource://database/613:1)
a+1 ----> 98
### 字符串的运算
加运算（相当于连接符而非运算符）
![70149d4672327278d5df7bc35d9a1a87.png](en-resource://database/617:1)
### 数值拆分
![649a399f6b72c302b09b4c3d13bd7acc.png](en-resource://database/616:1)
![c056e1276b8131f63d2f1fe8f6b117fa.png](en-resource://database/622:1)
![9e56d0be04d5386f378add303048bb20.png](en-resource://database/618:1)
### 自增自减、赋值运算
a++,   ++a
b--,      --b
![45782a011f88db69d385adf63c51e273.png](en-resource://database/623:1)
++在后：先运行程序操作，再自增
++在前：先自增，再运行程序操作
只能对变量进行操作，不能对常量进行操作

+= -+ *= /=（这里就不用强转了，也不会报错）
![7776e1e64ee8e31c7525a9fb4e2de1f5.png](en-resource://database/624:1)
![8c51b2330133bf969af9c30d2e963b8d.png](en-resource://database/625:1)
### 关系运算符、逻辑运算符
关系运算符返回结果只有true or false
![ad2405d3770e940cc93cfe23359fbc0c.png](en-resource://database/626:1)
![53d5336da1a73b565015ffe0b4ec3ef4.png](en-resource://database/627:1)
### 三元运算符
格式：关系表达式?表达式1: 表达式2
执行流程：
```mermaid
graph TD
A[计算关系表达式]  --> B{关系表达式的值}
B-->|true| D[取表达式1的值]
B -->|false| E[取表达式2的值]
```
## 条件控制语句
流程控制语句：通过一些语句来控制程序的**执行流程**
* 顺序结构：代码先后顺序依次执行
* 分支结构（if, switch）
* 循环结构(for, while, do...while)
### if语句
格式1：
    if(关系表达式){
        语句体;
        }
* 如果语句体只有一句，大括号可以省略（但不建议）
* 关系表达式后面不要加分号;，小括号大括号中间也不要加分号;

格式2：
    if(关系表达式){
        语句体;}else{
        语句体2;
        }
格式3：
    if(关系表达式){
        语句体;}else if{
        语句体2;
        }else if{
        语句体3;}else{
        语句体4;}
### switch语句
![219c34d16c39ac226175b3b7cd18bb7c.png](en-resource://database/628:1)
![2cb95135af5c9846fb3798a5b3e651b2.png](en-resource://database/629:1)
* case后面给的值不能重复，且只能是常量不能是变量

代码优化：case穿透
（我感觉没啥用，省略break只会一直运行下去（不管是否等于case的值）直到碰到break；整个就会变得很混乱，失去选择/开关功能）
![ef4f94be54c1f65bb7d941193c944eeb.png](en-resource://database/630:1)
在输出是相同的case上，可以适当省略代码。
## 循环
### for循环
![a6b7ab4ce1903be55f01e7ce299c45d9.png](en-resource://database/631:1)

关于打印: println是打印一行，print就是打印（不换行，无隔开）
### while循环
![3240968dbfb5160f534c56a2e5116310.png](en-resource://database/632:1)
不确定循环次数时常用while循环
### do...while循环
![b15a1e3050fc1a97df923b3b9a5cbbcc.png](en-resource://database/633:1)
不管条件是否满足，都会至少执行一次循环。
### 三种循环的对比、区别及应用场景
**for循环**
先判断后执行
for循环里定义的参数在结束循环后会消失
有明确的循环次数

**while循环**
先判断后执行
因为计数参数在循环外定义，所以循环结束后不会消失
无明确的循环次数

**do...while循环**
先执行后判断
很少用
### 死循环
ctrl+c强制停止循环 或 直接关掉cmd运行窗
应用场景例子：
键盘录入1-100之间的整数
顾虑：用户手动输入可能会产生错误
### 跳转控制语句
**continue**：跳过本次循环
**break**：结束整个循环
循环标号
![8b9b2aef3c8d29fde4ed7fa867c51b8b.png](en-resource://database/634:1)
## Random
![89bcda34fda6ef081618fedf2f5810e2.png](en-resource://database/1305:1)
## IDEA概述和安装
IntelliJ IDEA，业界公认目前JAVA开发最好的工具
![507110cc19078f73e59ddac066b1c637.png](en-resource://database/1307:1)
![18a135798ec3491f8eccfe6c70021722.png](en-resource://database/1309:1)
### 操作步骤
![e569bf77f8a1225b6f04841403194146.png](en-resource://database/1311:1)
编译自动完成，直接运行看结果就行
![a072c7bd62ff225b0f0a6795a8b2cdaf.png](en-resource://database/1313:1)
![b3b9052e53a262753d82da21eef4681f.png](en-resource://database/1315:1)
![c6e925493f0581938f80893066a941df.png](en-resource://database/1317:1)
![f4f9d88d4253aad1bc2d20c14ecf534b.png](en-resource://database/1319:1)
![7e29ee878dc92fa0451fa87adffb06ec.png](en-resource://database/1321:1)
![f648f5bab50e498d9402cae18ce9ee6a.png](en-resource://database/1323:1)
![47b4f84c36e89bf7606176f3a50d8d19.png](en-resource://database/1325:1)
![5e8cbf2a30c3d5bbf79c23a4d77ebb34.png](en-resource://database/1327:1)
![6c65e8a5b0bdc03b2b2a4531ad94e094.png](en-resource://database/1329:1)
![0d9ca14daa49748c9796a69635e4a38b.png](en-resource://database/1331:1)
![ae72c20315c344d8107be34a61dfe5a0.png](en-resource://database/1333:1)
![d5cde27007cc7fece4330c2ebb4c34a8.png](en-resource://database/1335:1)
![4c040702030ebca2dfee91c568ce9660.png](en-resource://database/1337:1)
![14b2c0eb689f051ad69944841a68e180.png](en-resource://database/1339:1)
### 快捷键
**psvm enter**
public static void main(String[] args) {    }

**sout enter**
System.out.println();

**alt + 1**
目录

**alt + 4**
控制台
![6410b5bb00186983fc5a452ec24e7046.png](en-resource://database/1341:1)
### IDEA操作项目和模块
![36dd4dd8d1bdee7b27dd69f262e4bcae.png](en-resource://database/1343:1)
## array数组
数组--存同种数据类型
数组类型和存储的数据类型保持一致
### 数组定义
格式一
数据类型[] 变量名
int[] array
格式二
数据类型 变量名[]
int array[]

空数组不能打印，得给它赋值。
### 数组初始化
**动态初始化**
数据类型[] 变量名 = new 数据类型[数组长度];
int[] arr = new int[3];
![e31afde7a3692b563c27e6d6af73572f.png](en-resource://database/1347:1)
运行结果：内存地址
![d429063b6edbaaa94b35f69ae8bed4b8.png](en-resource://database/1349:1)
![14b1c95e4065c54d53cccfdc57cc8186.png](en-resource://database/1351:1)
数组里的元素初始为零。

**静态初始化**
静态初始化：初始化时，就可以制订数组要存储的元素，系统还会自动计算出数组的长度。
格式：
数据类型[] 变量名 = new 数据类型[]{数据1，数据2，数据3，……};
int[] arr = new int[]{1,2,3,4,5};
或
数据类型[] 变量名 = {数据1，数据2，数据3，……};
int[] arr = {1,2,3,4,5};

| 初始化类型 | 特点 |
| --- | --- |
| 动态 | 明确数据个数，不明确具体数据 |
| 静态 | 已经明确具体数据 |

### 索引
* 从0开始
* 索引连续
* 逐一增加，每次加1
### 内存分配
![90f4308a1c9e3ae00ded3fc91763d8e4.png](en-resource://database/1353:1)
![a3b8d8bda93fbfa8ed4d1a7a63f4468b.png](en-resource://database/1355:1)
![29e365ab48032f406bcb842224ee1b5e.png](en-resource://database/1357:1)
两个数组内存图
![b2e7e091639787a15487835f1b84434b.png](en-resource://database/1359:1)
多数组指向相同内存图
![b2d849746f8a5fea923b408e28944ec4.png](en-resource://database/1361:1)
### 常见问题
**索引越界**
访问了不存在的索引
![793ddff4525c0ce65df2f7e38aff7b1d.png](en-resource://database/1363:1)
**空指针**
![9bfa7a1ebdc1c1d6ba8800f636d35352.png](en-resource://database/1365:1)
![a11e86b7a971a73ee9cd6814d0451e37.png](en-resource://database/1367:1)
### 遍历（取出数组所有数据）
动态获取数组元素个数
数组名.length
arr.length
### 二维数组
![41a81ceccb4fc5e5eb93b932b3687e6e.png](en-resource://database/1423:1)
![a6cf1eb01a3b861d13864069b538b933.png](en-resource://database/1425:1)
![826dce86ccb92f01ca85d0edf8825e06.png](en-resource://database/1427:1)
![7f97fb8ba614b9127bc0a77d475815b5.png](en-resource://database/1429:1)
## 方法method和debug
内容：定义和调用，形参和实参，返回值，通用格式，重载，参数传递，debug。
方法（method）:一段具有独立功能的代码块，不调用就不执行。（JAVA里没有函数，方法就是函数的作用）

* 方法必须先创建才可以使用，该过程成为方法的定义
* 方法创建后并不是直接运行，需要手动使用后再执行，该过程成为方法的调用
* 方法不能嵌套使用
* 方法返回值为void代表没有返回值
* return之后的代码不执行（方法结束/弹栈）
![cdc19d3645dd9d82c03f1bf27534bbfe.png](en-resource://database/1375:1)
![5b77756351d15c8d91483dcd8a4b1ac7.png](en-resource://database/1377:1)
定义在public static void main之外，public class内。
* 方法没有被调用的时候，都在方法区中的字节码文件（.class）中存储
* 方法被调用的时候，需要进入到栈内存中运行（栈内存：先进后出）
![616d02dcf96c28d4b9a7bad4cdf9ed9b.png](en-resource://database/1379:1)
### 参数的引入
![fa51b37da810bd5ccda8e417c86f429c.png](en-resource://database/1383:1)
形参：形式参数，指方法定义中的参数（指代的字母）
实参：实际参数，指方法调用中的参数（实际数字）
### 返回值
![ebbb0792d824e75cec920820e2a00cda.png](en-resource://database/1385:1)
同时注意得有一个变量在main块里去接受return的值;
return只能返回一个结果，不过可以返回一个数组
![a20061c5ab0fa9fe9569bd754eb7ba0a.png](en-resource://database/1387:1)
### 重载
同一个class中可以存在同名的method（但不允许input也相同），通过参数的不同类型或参数个数或参数顺序来确定和选择不同的method。
包括打印这个method也是用了很多针对不同数据类型的重载。
![75879e112b077fb8db630660d3171475.png](en-resource://database/1389:1)
### 参数传递
如果input是数组的一个值的话，修改之后对数组的值本身会改变
### debug
断点（鼠标左键点一下），debug模式运行。
## 进制
### 进制介绍
计算机数据在底层运算的时候都是以二进制。
**十进制**
逢十进一
**二进制**
0+1 逢二进一 
0011+1 = 0100
![e2a1c2e996312aa204f3dda6e54a2d9c.png](en-resource://database/1395:1)
![0857720bea288177b2226b6fc2eac169.png](en-resource://database/1397:1)
在jdk7版本之后是这样，之前可能会不一样。
### 进制转换
![81d3370048f7fee8beeeade4140c534b.png](en-resource://database/1403:1)
![349b18e8cfdcccb5f38f0d047d7f4461.png](en-resource://database/1405:1)
8421码
![02773c5ce4ed71a21f19b4f868ef4a1c.png](en-resource://database/1407:1)
![c4bdef9c19850b604d1b3fbee2e05914.png](en-resource://database/1409:1)
![e5dd6268b6295cded7d885bf0aebd0f8.png](en-resource://database/1411:1)
### 原码反码补码
计算机中的数据都是以二进制补码的形式在运算，而补码则是通过反码和源码推算出来的。
原码：可直观看出数据大小（看数据）
反码：（转数据）
补码：数据以该形态进行运算（运算数据）
![8eeaed00420cba8cd905ad423c5df4a5.png](en-resource://database/1413:1)
![855e6d0c63bd26f7691748fc6183172c.png](en-resource://database/1415:1)
### 位运算符
![0cab8837139b4bff843fa261fc350f6f.png](en-resource://database/1417:1)
a ^ b ^ b = a
![72fdd4eb1632934268ae346c763b5c8a.png](en-resource://database/1421:1)
### 数据交换
![6eefca068669457959d7d18424888dec.png](en-resource://database/1419:1)
# 面向对象
面向对象：以对象对中心，通过指挥对象实现具体的功能；
面向过程：以过程为中心，实现功能的每一步，都是自己实现的

类：类是对现实生活中一类具有共同属性和行为的事物的抽象（对对象的一种描述，可以将类理解为一张设计图；根据设计图，可以创建出具体存在的事物）
根据类去创建对象

## 类的组成：
* 属性（该事物的各种特征）
* 行为（该事物存在的功能，能够做的事情）

## 类和对象的关系
类：类是对现实生活中一类具有共同属性和行为的事物的抽象
对象：是能够看得到摸得着的真实存在的实体

类是对象的描述
对象是类的实体
## 类的定义
![aa51ce064ab1c7e08075be6eb89470ef.png](en-resource://database/1439:1)
## 对象的创建和使用
![f974110bfb963f48083b17141fb31645.png](en-resource://database/1441:1)
对象的创建和类的定义不一定在同一个文件里进行
定义类后，所有的初始值都为0.
## 对象内存图
### 单个对象
![91056fb4f250be32aa28501af1c63201.png](en-resource://database/1443:1)
### 两个对象
![0f4288247ab0629308223a79eec029ba.png](en-resource://database/1445:1)
![d0c9c5b2e648ed180cb945b05c64380e.png](en-resource://database/1447:1)
### 由两个引用指向同一个对象
![e07ee3a6a640e30695dbc34d0bf1149f.png](en-resource://database/1449:1)
![6f0c5ee863b909347b4c4d242d9caf2f.png](en-resource://database/1451:1)
## 成员变量 局部变量
成员变量：class中method外的变量
局部变量：method里的变量
![b3f9222721f344861a1ed956d9db1b14.png](en-resource://database/1453:1)
## private
![7b685034bd71aad0fcece0c7406e14b7.png](en-resource://database/1455:1)
加上private之后就关闭了直接调用的通道(student.age)（只在该class里有效），用method进行赋值，在方法里可以写一个条件判断以筛选合适的输入值
之后所有的成员变量都私有化，
## this关键词
成员变量/方法和局部变量/方法名字相同（就近原则）。在this.之后的变量为成员变量。
![ff6a5f0f207f51c4ddc6c1508c22d99e.png](en-resource://database/1457:1)
![77ee92759375cc6623aac1f42065d447.png](en-resource://database/1459:1)
![0b8a31bbc59196f52ecc2793e58900fe.png](en-resource://database/1461:1)
## 封装
面向对象三大特征之一（封装、继承、多态）
隐藏实现细节，仅对外暴露公共的访问方式
private就是封装的一种体现
## 构造方法
![a4cb2aa24bb00ce185a3db08bcfb8e64.png](en-resource://database/1463:1)
在创建对象的时候就会运行一遍构造方法，不需要任何手动调用，也不能被手动调用；每创建一次对象都会运行一遍构造方法。
![c994a6c693e6099a14c5b809685b9e5b.png](en-resource://database/1465:1)
作用：在创建对象的时候给对象赋值
![306bc02b896d9113d6d8396d807cd811.png](en-resource://database/1467:1)

注意事项
1. 构造方法的创建（如果没有定义构造方法，系统将给出一个默认的无参数构造方法；如果定义了构造方法，系统将不再提供默认的构造方法）
2. 构造方法的重载（如果自定义了带参数的构造方法，还要使用无参数的构造方法，就必须再写一个无参数的）
3. 推荐的使用方式（无论是否使用，都手动写无参数的构造方法和带参数的构造方法）
![9f0fc4f7079005dce193fcf24ae7c844.png](en-resource://database/1481:1)
## 标准类
![66d494d0112853e2122e287eb1a31c08.png](en-resource://database/1469:1)
# API基础
API: application programming interface应用程序编程接口。
厂商提供给应用程序编程的接口（提前写好的类）
java API: 指JDK中提供的各种功能的java类（通过帮助文档来学习）
![2ec24b05216db591253ba4538290fb21.png](en-resource://database/1549:1)
![23343ab55ad2f3b6f3102e9c3084cac6.png](en-resource://database/1551:1)
## String类
![6540d6e7503f409cc245cdd1f36bddcb.png](en-resource://database/1553:1)
String类在lang包下，是主包，如果在lang下就不用手动调取了
只要是双引号定义的，就是一个string对象
![4c09c4799d4790781d986d0d8ef7fc5d.png](en-resource://database/1555:1)
字符串是常量，其值在创建之后不能更改。
![9c9e2d75b22cec814872a176e3f9b44e.png](en-resource://database/1557:1)
![e24351330f72cf5537a3bae74882b605.png](en-resource://database/1559:1)
### String常见构造方法
![5fdc2d22895a431cc613a2158e76cd1d.png](en-resource://database/1561:1)
![dcb86dc3fd80cd307177f63595738d60.png](en-resource://database/1563:1)
### 创建字符串对象的区别对比
创建字符串对象的方法：
1. 构造方法
![715a7cf150d90ed5c72a9d834fc7965b.png](en-resource://database/1567:1)
2. 双引号
![43b3d43e9556f57289da08d4c67417e5.png](en-resource://database/1565:1)
双引号创建的字符串对象，在字符串常量池中储存；通过构造方法创造的字符串对象，在堆内存中储存
![730adb4b277354fd31b5d13386a0889c.png](en-resource://database/1569:1)
### String特点
* Java程序中所有的双引号字符，都是string类的对象
* 字符串不可变，它们的值在创建后不能被更改
* 虽然string的值是不可变的，但是它们可以被共享

常见面试题
1.
![b15026cfa737de17d5bb6b6455cb5668.png](en-resource://database/1571:1)
2. 
![0a743f08e22a12add047a05310acf92f.png](en-resource://database/1573:1)
3.
![b948c73da54e9f64596371283c5dc376.png](en-resource://database/1575:1)
当字符串使用+号连接的时候，系统底层会自动创建一个stringbuilder对象然后再调用其append方法完成拼接。拼接后，再调用其toString方法转换为string类型。
![49f2312be543e649490f4007957252bc.png](en-resource://database/1577:1)
4.
![852fb25f89d09e76c2687ae0e24409b5.png](en-resource://database/1579:1)
Java存在常量优化机制，这里的单个字符就是常量。在编译的时候，就会将"a"+"b"+"c"拼接为"abc"
### 字符串的比较
![472da9697749d5664235352d622cc6c0.png](en-resource://database/1581:1)
![60759a2328938e35266ef609a1bb3a88.png](en-resource://database/1583:1)
### 字符串处理
![642dee3e68d96e19cbb1e9006f1e31c4.png](en-resource://database/1585:1)
## Stringbuilder
StringBuilder是一个可变的字符串类（与不可变的String常量不同）
作用：提高字符串的操作效率(运行时间比string更快)
链式编程
![2420ac7fc147b31f0f87ef5cf78a2293.png](en-resource://database/1593:1)
![1ea3af457b305da52a8d59b4b82bead3.png](en-resource://database/1597:1)
![b61e38c74810e5cc0941f05a6282c2a5.png](en-resource://database/1599:1)
# 集合基础
![5b6b07582c1fa6497c7ff6d2b00cd7a6.png](en-resource://database/1609:1)
![29dd181f43ce3f46850e9935c3bc1a9f.png](en-resource://database/1611:1)
![e152cba4e63f132dc8e8dc0747f6c04e.png](en-resource://database/1613:1)
