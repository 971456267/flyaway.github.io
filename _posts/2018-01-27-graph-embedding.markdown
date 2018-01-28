---
layout:	post
title:	Graph Representation Learning
date:	2018-01-27
categories:	Embedding
tags:	Embedding

---

本文根据王鸿伟博士分享整理，参考博文在文末~　　
## 概述
Graph Representation Learningz（GRL）中文可称之为图特征学习或者网络特征学习，其主要目的在于，将图中每个节点
映射到一个低维向量空间，并且在此空间保持原有图的结构或者距离信息。其应用十分广泛，它可以被用于链路预测，
节点分类，推荐系统，视觉，知识图谱，聚类，Text Embedding以及社会网络分析。　　

## GRL分类
### 按输入分类
1. Homogeneous graph(同构图)：Weighted/Unweighted, Directed/Undirected, Signed/Unsigned
2. Heterogeneous graph(异构图): Multimedia network, knowledge graph
3. Graph with side information: Node/edge label(categorical), Node/edge attribute(discrete or continuous),Node feature(e.g.,texts)

### 按输入分类
1. Node embedding(the most common case)
2. Edge embedding: Relations in knowledge graph, link Prediction
3. Sub-graph embedding: Substructure embedding, Community embedding
4. Whole-graph embedding: Multiple small graphs, e.g., molecule,protein

### 按方法分类
1. Matrix factorization, Singular value decomposition(奇异分解), Spectral decomposition(eigen-decomposition，特征分解)
2. Random walk, 14年的论文，就是将了使用随机游走的方式产生路径，将路径看作是nlp里面的sentences，然后使用word embedding的方法（skip-gram,cbow）进行embedding，将图中的节点使用低维连续向量进行表示，是无监督学习。
3. Deep learning，Auto-encoder, CNN
4. self-defined loss: Maximizing edge reconstruction probability, Minimizing distance-based loss, Minimizing margin-based ranking loss(这种方法常见于知识图谱)

## 表示学习方法演变
<img src="/assets/images/represent_work.webp" style="vertical-align: center" height = '350' width = '500'>

## GraphGAN

### motivation
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js config=TeX-AMS-MML_HTMLorMML">
</script>
 $$n=x$$

1. generative graph representation通过假设潜在真实的连接
## 参考博文
[参考博文链接](https://mp.weixin.qq.com/s?__biz=MzAwMTA3MzM4Nw==&mid=2649442783&idx=1&sn=7263a483b50ac01ca29c8ee07caa852b&chksm=82c0a05bb5b7294d7bfa8b1d5522a21cc126825f3eeb0428c7551452b0437e13182d102b0945&mpshare=1&scene=1&srcid=0126soOPoxQ7XHZLcdoczNaO&pass_ticket=yIy0ZoUQtNvMGxVSUAzPrkUXE%2BtaloSw5d%2F5cftsrC9vmz0LNCmm3kltg%2BCwHthI#rd)



