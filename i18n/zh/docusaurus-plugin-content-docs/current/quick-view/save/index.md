---
sidebar_position: 3
title: 保存任意形状
---

保存指令是Jimmer一个非常强大的能力，只需一个函数调用，即可保存任意形状的数据结构。

无论被保存的数据结构简单也罢 *(比如，孤单对象甚至残缺对象)*，复杂也罢 *(一个聚合根对象通过关联关系持有很多关联对象，深度和广度不受限制)*，都可以使用一个函数调用将它存入数据库。

:::tip
单表记录的保存操作从来不是应用开发的难点，即使不使用任何ORM框架，直接使用JDBC也是非常容易实现的。

然而，保存复杂的数据结构却很不容易，开发人员将不得不从数据库中查询现有数据结构，和即将保存的数据结构对比，从而发现有变化的多个局部，并转化为相应的`INSERT`、`UPDATE`和`DELETE`语句，这个过程非常繁琐且容易出错。

因此，自一开始，Jimmer就着眼于如何保存复杂的数据结构，而非如何保存一个孤单的实体对象。
:::