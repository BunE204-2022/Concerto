在Concerto平台中，创造一个新的节点(node)一般需要由两部分组成：Wizard和Source test。如下图所示，系统自带的assessment节点由Wizard assessment与Source test _assessment两部分组成。  

![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/1.png)

## 以创建能够储存作答者身份标签至响应表格的节点(node)为例
将该节点命名为myassessment，创建该节点分为以下三步
### 1. Source test _myassessment  

在Test/Starter content中复制_assessment为_myassessment，_myassessment会出现在Test/User made中，其主要由两部分组成：Test flow与Test input。Test flow可将其想象为神经网络，每一个节点想象成神经元，神经元上由输入、输出以及两者之间的关系函数(code)。那么Test input表示初始化输入的变量，也即神经网络输入层所输入的变量。  

![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/2.png)

 1. login输入
    在Test input中创建新变量，命名为login
    ![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/3.png)
 2. 将login设置为全局变量
    在Test flow中的第一个神经元，即输入层找到login，点击它并将其设置为Flow variable pointer
    ![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/4.png)
 3. 在create settings和response processer中添加login输入(显示为蓝色，显示为红色的为输出)，并将其设置为Flow variable pointer
    ![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/5.png)
    ![image](https://github.com/BunE204-2022/concerto/blob/main/%E5%88%9B%E9%80%A0%E6%96%B0%E8%8A%82%E7%82%B9/images/6.png)
 4. 在response processer中修改代码
    见login.r文件
### 2. Wizard myassessment


### 3. node myassessment
