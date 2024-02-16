# map

https://cloud.tencent.com/developer/article/1680352

## 注意点：

```C++
map<int,int> hash;
hash[1];
//这里的hash[1],会去访问键值为1的 key-value。分两种情况：
//如果不存在键值1，则创建一个key为1，value为0的默认键值对存于hash中
//如果存在键值1，则访问key为1对应的value
```

