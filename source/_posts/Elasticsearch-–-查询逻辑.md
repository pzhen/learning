---
title: Es - 查询逻辑
toc: true
comments: true
share: true
date: 2017-09-27 14:39:11
tags:
 - Elasticsearch
 - Es
categories:
 - Elasticsearch
---

查询发送到Elasticsearch的其中一个节点，这时发生的是一个所谓的发散阶段。查询分布到<!-- more -->
建立过索引的所有分片上。如果它建立在5个分片和1个副本基础上，那么，这5个实体分片都会
被查询(不需要同时查询分片及其副本，因为它们包含相同的数据)。每个查询的分片将只返回
文档的标识符和得分。发送分散查询的节点将等待所有的分片完成它们的任务，收集结果并适当 排序(在这种情况下，按得分从低到高)。

之后，将发送一个新的请求来生成搜索结果。
然而，这次请求将只发送到那些持有响应所需 文档的分片上。
在大多数情况下，Elasticsearch不会把请求发送到所有的分片，而只是发送给其中的一部分。
这是因为通常不需要整个查询结果，只要一部分。
这一阶段被称为收集阶段(gather phase)。
收集完所有文档，将建立最终响应，并返回查询结果。

当然，上述是Elasticsearch的默认行为，可以改变。

