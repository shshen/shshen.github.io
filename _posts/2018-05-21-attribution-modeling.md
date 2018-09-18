---
layout: post
title:  "实时数据分析"
subtitle: "归因分析介绍和Api设计"
author: "Shane"
date:   2018-05-21 14:50:45
---
> 作为实时数据分析系列的第一篇，我一直纠结于该选那个题目。按照正常的逻辑，应该由浅入深，先讲一下一些基本概念，诸如dimension，metric，filter，evar等等。或者对业内主流分析工具做一下比较，如Google Analytics，Druid和Adobe Analytics之类。再或者讲一下主流的系统架构。 而我选择归因分析的主要原因就是因为其功能强大，国内的分析工具普遍支持不好，并且网络上很难一个清晰的api设计。


| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |


```shell
curl 'http://localhost:9096/report?suite=pagevoice&dimension=age&metric=pageviews&session=30&interval=20171007d10'
```

```json
{
  "dimension": "age",
  "metric": "pageviews",
  "results": {
    "27": 8,
    "18": 2,
    "32": 1
  },
  "code": 200,
  "time": 2
}
```