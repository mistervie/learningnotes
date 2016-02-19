# 关于KVC
###使用方法
- 创建一个模型类 如xxx
- 声明模型类中所需要的属性，和数据字典中的Key值一一对应
- 在h文件中声明 +(instancetype)xxxWithDic:(NSDictionary *)dic 方法
- 在m文件中实现 +(instancetype)xxxWithDic:(NSDictionary *)dic 方法

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
