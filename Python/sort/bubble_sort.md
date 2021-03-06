### 1.1 Python 冒泡排序算法
#### 1.1.1 概述

冒泡排序算法是最简单的排序算法，如果顺序错误，可以反复交换相邻的元素来实现排序。
#### 1.1.2 算法描述
```text
//冒泡排序1
void BubbleSort1(int a[], int n)
{
    int i, j;
    for (i = 0; i < n; i++)
        for (j = 0; j < n - i - 1; j++)
            if (a[j] > a[j + 1])
                Swap(a[ j ], a[j + 1]);
}
```
#### 1.1.3 语言描述
冒泡排序原理: 每一趟只能将一个数归位， 如果有 n 个数进行排序，只需将 n-1 个数归位， 也就是说要进行 n-1 趟操作(已经归位的数
不用再比较)。冒泡排序虽然解决了桶排序浪费空间的问题， 但是冒泡排序的效率特别低。

#### 1.1.4 Example

##### 冒泡排序动态图示

![bubble_sort](../images/Bubble-sort-example-300px.gif)

#####一次正常的冒泡算法描述如如下：

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

现在，数组已经排序，但算法不知道它是否已排序完全。

第三次通过：

（**1** **2** 4 5 8） - >（**1** **2** 4 5 8）

（1 **2** **4** 5 8） - >（1 **2** **4** 5 8）

（1 2 **4** **5** 8） - >（1 2 **4** **5** 8 ）

（1 2 4 **5** **8**） - >（1 2 4 **5** **8**）

##### 动态图示
##### 考虑递归实现
使用递归冒泡排序并没有性能/实现上的优势，但有助于理解冒泡排序以及递归思想。因为将循环化为递归，避免不了“方法压栈”的现象出现。

现在来考虑冒泡排序算法，根据以上的例子部分，在第一遍中，算法将最大的元素移动到数组最后的位置（按递增顺序），在第二遍中，算法将第二大的元素放置在倒数第二的位置，依次类推。

**一种递归思想：**

    1.基本情况：数组大小为 1，返回
    2.做一次正常的冒泡排序。此过程调用递归算法
    3.递归子数组


【相关推荐】
+ [5.7. The Bubble Sort¶](http://interactivepython.org/runestone/static/pythonds/SortSearch/TheBubbleSort.html)