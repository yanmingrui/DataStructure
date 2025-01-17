## 二叉搜索树

### 定义
- 左子树节点值比父节点小
- 右子树节点值比父节点大


### 性质
平均查询时间复杂度为O(logn)，最坏时间复杂度为O(n)。原因是构建树的过程，有可能退化成链表，最终树的形状与输入顺序有关。

### 操作
1. 插入
2. 删除
3. 查询

这里主要说前两种
#### 插入
插入的节点只能作为叶子节点
1. 比当前值大，插入到右子树中
2. 比当前值小，插入到左子树中
3. 相等，已经存在，不用插入

#### 删除
删除分为三种情况
1. 出度为0，直接删除
2. 出度为1，将孩子挂在当前节点
3. 出度为2，删除左子树中最大的节点值，并用这个最大值替换欲删除节点的值


![xxx](https://img-blog.csdnimg.cn/20210519092332562.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzMwMTI0MjQx,size_16,color_FFFFFF,t_70)
如图所示
