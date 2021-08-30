# ES

## kibana链接es

Kibana有默认的ES连接地址，如果不是本地地址，则需要修改kibana的配置去连接ES。



## es集群

es集群后再head创建索引后主分片和副本会被分配到不同的es节点上，主分片可读可写，副本只能读。

分片三个状态：未分配，初始化，迁移中。

集群三种状态：都可用则绿色，只有副本不能用黄色，主分片不能用红色。



## 倒排索引

把一个字段结果里的词单独在另一个表作为字段，然后字段右边是第一个表的id（那些包含这些词）



### 前缀树

![image-20210826133208635](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826133208635.png)



![image-20210826133530642](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826133530642.png)

缺点：后面出现一样的不能进行压缩



### FSM

![image-20210826133939673](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826133939673.png) 



### FSA

![image-20210826134255518](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826134255518.png)

![image-20210826134328126](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826134328126.png)



### FST

![image-20210826140716551](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826140716551.png)



![image-20210826140829227](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826140829227.png)



![image-20210826141845052](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826141845052.png)

![image-20210826141858209](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826141858209.png)

![image-20210826141800902](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826141800902.png)







![image-20210826184448480](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210826184448480.png)  



git资料

![image-20210830132202154](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830132202154.png)

## 中文分词器

### 安装

![image-20210830132356722](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830132356722.png)

下载后把里面的东西全部放到ik里

![image-20210830132459644](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830132459644.png)

### 词库

![image-20210830132825916](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830132825916.png)

遇到没有的词可以自己配置

![image-20210830133143757](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830133143757.png)



### 热更新

![image-20210830135923873](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830135923873.png)

![image-20210830133702729](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830133702729.png)

#### 基于远程词库

![image-20210830135521383](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830135521383.png)

#### 基于mysql

![image-20210830141029552](C:\Users\blackMamba\AppData\Roaming\Typora\typora-user-images\image-20210830141029552.png)

