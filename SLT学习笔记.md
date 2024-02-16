# map

https://www.cnblogs.com/fnlingnzb-learner/p/5833051.html

https://cloud.tencent.com/developer/article/1680352

## 注意点：

- 使用数组下标取值

  ```C++
  map<int,int> hash;
  hash[1];
  //这里的hash[1],会去访问键值为1的 key-value。分两种情况：
  //如果不存在键值1，则创建一个key为1，value为0的默认键值对存于hash中
  //如果存在键值1，则访问key为1对应的value
  ```

- 排序问题

  - map的内部是基于红黑树进行实现的，红黑树，是一种不严格平衡二叉树，平衡二叉树的前提是二叉搜索树，具体可见，红黑树的具体讲解：https://www.cnblogs.com/crazymakercircle/p/16320430.html
  - 在遍历map的时候，一般默认得到的是，按键值升序排序的key-value。
    - 因为map内部是红黑树，也是一种自平衡的二叉搜索树，遍历map的时候，本质上的实现是对红黑树进行中序遍历，从而获得升序数据。获得有序数据最关键的还是利用了中序遍历二叉搜索树这个性质。
  - 对于红黑树性质的利用，主要还是考虑到查找，插入，删除时的效率，都是O(logn)

