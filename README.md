# Task 1 知识图谱介绍 学习笔记

> 文章编写人：Chris Van<br/>

## 目录

- [目录](#目录)
- [一、知识图谱简介](#一知识图谱简介)
  - [1.1 引言](#11-引言)
  - [1.2 什么是知识图谱呢？](#12-什么是知识图谱呢)
    - [1.2.1 什么是图（Graph）呢？](#121-什么是图graph呢)
    - [1.2.2 什么是 Schema 呢？](#122-什么是-schema-呢)
  - [1.3 知识图谱的价值在哪呢？](#13-知识图谱的价值在哪呢)
- [二、怎么构建知识图谱呢？](#二怎么构建知识图谱呢)
  - [2.1 知识图谱的数据来源于哪里？](#21-知识图谱的数据来源于哪里)
  - [2.2 信息抽取的难点在哪里？](#22-信息抽取的难点在哪里)
  - [2.3 构建知识图谱所涉及的技术？](#23-构建知识图谱所涉及的技术)
  - [2.4、知识图谱的具体构建技术是什么？](#24知识图谱的具体构建技术是什么)
    - [2.4.1 实体命名识别（Named Entity Recognition）](#241-实体命名识别named-entity-recognition)
    - [2.4.2 关系抽取（Relation Extraction）](#242-关系抽取relation-extraction)
    - [2.4.3 实体统一（Entity Resolution）](#243-实体统一entity-resolution)
    - [2.4.4 指代消解（Disambiguation）](#244-指代消解disambiguation)
- [三、知识图谱的存储](#三知识图谱的存储)
- [四、Neo4J 介绍与安装](#四neo4j-介绍与安装)
  - [4.1 引言](#41-引言)
  - [4.2 Neo4J 下载](#42-neo4j-下载)
  - [4.3 Neo4J 安装](#43-neo4j-安装)
  - [4.4 Neo4J Web 界面 介绍](#44-neo4j-web-界面-介绍)
  - [4.5 Cypher查询语言](#45-cypher查询语言)
- [五、Neo4J 实战](#五neo4j-实战)
  - [5.1 引言](#51-引言)
  - [5.2 创建节点](#52-创建节点)
  - [5.3 创建关系](#53-创建关系)
  - [5.4 创建 出生地关系](#54-创建-出生地关系)
  - [5.5 图数据库查询](#55-图数据库查询)
  - [5.6 删除和修改](#56-删除和修改)
- [六、通过 Python 操作 Neo4j](#六通过-python-操作-neo4j)
  - [6.1 neo4j模块：执行CQL ( cypher ) 语句](#61-neo4j模块执行cql--cypher--语句)
  - [6.2 py2neo模块：通过操作python变量，达到操作neo4j的目的](#62-py2neo模块通过操作python变量达到操作neo4j的目的)
- [七、通过csv文件批量导入图数据](#七通过csv文件批量导入图数据)
- [参考资料](#参考资料)


## 一、知识图谱简介

### 1.1 是什么？

本质上是语义网络（Senmantic Network）的知识库，可以简单理解成多关系图（Multi-relational Graph）。

多关系图：包含多种类型的节点（Vertex）和多种类型的边（Edge）,节点代表现实世界中的事物实体，边则代表实体之间的某种联系。

模式（Schema）：限定了知识图谱的数据格式，包括实体对象（Thing）及其值的类型（DataType），实体对象是某个领域内有意义的概念。

![Schema定义.PNG](https://i.loli.net/2020/12/06/zxMLupBIewb2jFR.png)







