# 关于KVC
###使用方法
1. 创建一个模型类 如xxx
2.	在h文件中声明 +(instancetype)xxxWithDic:(NSDictionary *)dic 方法
3.  在m文件中实现 +(instancetype)xxxWithDic:(NSDictionary *)dic 方法

```objc	
+(instancetype)xxxWithDic:(NSDictionary *)dic{
    Xxx *wi = [[Xxx alloc]init];
    [wi setValuesForKeysWithDictionary:dic];
    return wi;
}
```
###字典转模型
```objc
NSDictionary *dic = [NSDictionary dictionary];
//或者从网络获取的数据字典
Xxx *x = [Xxx xxxWithDic:dic];
```
