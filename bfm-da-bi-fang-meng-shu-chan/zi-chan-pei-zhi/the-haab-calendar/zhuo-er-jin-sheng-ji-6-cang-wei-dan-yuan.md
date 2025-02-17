# 哈布历法3——仓位单元，量子调仓

## [The two types of Altcoins, an investor's view](https://woobull.com/the-two-types-of-altcoins-an-investors-view/)

振荡型 和 衰减型 的区别

{% hint style="info" %}
### 哈布历 5.04 —— 增加了派网驾驶舱，增加了比例换算尺和仓位单元

### **我发明了一种屯币宝用法，就是量子调仓，按照市值排名选择自己喜欢了解的代币，然后按照币优的市值排名，分配进以10%或者5%为单位的量子仓位里面。等到排名改变再修改仓位。**

### **这样就克服了屯币宝仓位的选择恐惧症。**

原驾驶舱更名为币安驾驶舱。

[卓尔金+哈布飞船5.04](https://share.weiyun.com/F5Zb2drW)
{% endhint %}

## 粗略固定的量子调仓

![](<../../../.gitbook/assets/屏幕快照 2021-09-02 下午3.52.15.png>)

## 精确的量子调仓

精确的量子调仓由4部分组成：

1，根据[市值占比修正幂率](../the-tzolkin-calendar/zhuo-er-jin-sheng-ji-10-shi-zhan-mi-xiu.md)后的仓位比例进行[银行家舍入](https://www.ituring.com.cn/article/35304)

2，根据数量扩充单元格&#x20;

[EXCEL中如何根据指定数量扩充单元格](https://jingyan.baidu.com/article/922554461774d1851648f4da.html)

3，换行，分组到多行&#x20;

[不仅仅是做图表，用EXCEL排会议座位图你试过么？](https://baijiahao.baidu.com/s?id=1664682492776373374)

[再只会单一升降排序就OUT了，教你三种EXCEL中的数字排列](https://baijiahao.baidu.com/s?id=1664500298511765341)

4，相同的单元格显示相同的颜色。

[如何让EXCEL相同的单元格显示一样的颜色](https://zhidao.baidu.com/question/1644347434384497340.htm)

[excel怎么把相同的字符，标记为一个颜色](https://zhidao.baidu.com/question/2138014715383739028.html)

### [银行家舍入算法](https://www.ituring.com.cn/article/35304)（四舍六入五取偶）

```python
=IFS(MOD(C25,D25)<D25/2,C25-MOD(C25,D25),
     MOD(C25,D25)>D25/2,C25-MOD(C25,D25)+D25,
     MOD(C25,D25)=D25/2,IFS(
                            MOD(C25,2*D25)=0.5*D25,C25-MOD(C25,2*D25),
                            MOD(C25,2*D25)=1.5*D25,C25-MOD(C25,2*D25)+2*D25
                           )
    )
```

