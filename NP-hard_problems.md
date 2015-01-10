# Problem: Multicut on Trees

## description：
给定一颗树T和一个点对集合R={(u1,v1)...(ur,vr)}，删除k条边使得所有点对不连通（砍断所有路径）

reference：
《Algorithms For Cut Problems On Trees》


# Problem: Multiway cut on Trees

## description：
给定一颗树T和一个点集S={v1...vs}，删除k条边使得所有点对（vi,vj）之间没有通路（不连通，或曰砍断所有路径）

reference:
《Algorithms For Cut Problems On Trees》

# Problem: steiner tree(斯坦纳树)

## description:
给一个无向图和一个点集S，做一棵包含S的生成树，使其cost最小。

## Algorithm:

近似算法：
1.Kou Markowsky and Berman algorithm
step 1.
用Floyed算法求最短路，构造一个新的图G1，G1中边(u,v)的cost设为原图(u,v)的最短路径长度
step 2.
在G1中做最小生成树T
step 3.
把T中的边用原图G中对应的路径代替，删除环
算法效率：n三次方，近似率为2。
