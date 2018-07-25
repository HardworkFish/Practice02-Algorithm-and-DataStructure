###### 1.1 Python 冒泡排序算法
#### 1.1.1 概要

冒泡排序算法是最简单的排序算法，如果顺序错误，可以反复交换相邻的元素来实现排序。

#### 1.1.2 Example

第一遍：

（**5** **1** 4 2 8） - >（**1** **5** 4 2 8），这里，算法比较前两个元素，交换自5> 1

（1 **5** **4** 2 8） - >（1 **4** **5** 2 8），交换自5> 4 

（1 4 **5** **2** 8） - >（1 4 **2** **5** 8），交换自5> 2 

（1 4 2 **5** **8**） - >（1 4 2 **5** **8**），现在，由于这些元素已经按顺序排列（8> 5），算法不会交换它们。

第二次通过：

（**1** **4** 2 5 8） - >（**1** **4** 2 5 8）

（1 **4** **2** 5 8） - >（1 **2** **4** 5 8），交换4> 2 

（1 2 **4** **5** 8） - > （1 2 **4** **5** 8）

（1 2 4 **5** **8**） - >（1 2 4 **5** **8**）

现在，数组已经排序，但我们的算法不知道它是否已完成。该算法需要一个完整的传递，没有任何交换，知道它已经排序。

第三次通过：

（**1** **2** 4 5 8） - >（**1** **2** 4 5 8）

（1 **2** **4** 5 8） - >（1 **2** **4** 5 8）

（1 2 **4** **5** 8） - >（1 2 **4** **5** 8 ）

（1 2 4 **5** **8**） - >（1 2 4 **5** **8**）