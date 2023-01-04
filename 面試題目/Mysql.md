# mysql

[Data Structure Visualization](https://www.cs.usfca.edu/~galles/visualization/Algorithms.html)

### B树和B+树之间的区别是什么？
https://www.cs.usfca.edu/~galles/visualization/BTree.html


### 以下是一些可能使用此類索引的查詢示例：

SELECT * FROM demo_table WHERE column [ = | > | >= | < | <= ] 'value';
SELECT * FROM demo_table WHERE column_a BETWEEN 100 AND 200;
SELECT * FROM demo_table WHERE column LIKE 'value%';

### MySQL 中的覆蓋索引
SELECT column_1, column_2 FROM demo_table WHERE column_3 = 'value';

---
index 16 kb
b+ tree
data page
雙向
目錄+數據

主鍵 : 插入時候，需要先排序
聯合index
最左原則
類型相同
where ， order by
索引覆蓋 
回表
where a+1 = 5 ， 無法走索引
聯合索引 : 1 ? 1  




---


Innodb中的B+树是怎么产生的？
高度为3的B+树能存多少条数据？ 千萬級別
Innodb是如何支持范围查找能走索引的？
为什么要遵守最左前缀原则才能利用到索引？
范围查找导致索引失效原理分析
覆盖索引的底层原理
索引扫描底层原理
order by 为什么会导致索引失效？
mysql中的数据类型转换有哪些要注意的？
对字段进行操作导致索引失效原理



Mysql中有哪些存储引擎？
03:13
P14
MyISAM和InnoDB的区别是什么？
02:21
P15
数据表设计时，字段你会如何选择？
03:27
P16
Mysql中VARCHAR(M)最多能存储多少数据？
01:06
P17
请说下事务的基本特性？
01:08
P18
事务并发可能引发什么问题？
02:53
P19
简单描述下Mysql各种索引？
02:49
P20
什么是三星索引？
01:41
P21
InnoDB一颗B+树可以存放多少行数据？
02:59
P22
如何提高insert的性能？
03:57
P23
什么是全局锁、共享锁、排它锁？
01:58
P24
谈一下Mysql中的死锁
02:34
P25
Mysq如何实现读写分离
03:23
P26
Mysq如何实现分库分表
04:34
P27
索引的基本原理
07:19
P28
mysql聚簇和非聚簇索引的区别
15:23
P29
mysql索引结构，各自的优劣
08:37
P30
索引的设计原则
06:04
P31
mysql锁的类型有哪些
12:34
P32
mysql执行计划怎么看
14:24
P33
事务的基本特性和隔离级别
21:02
P34
怎么处理慢查询
04:40
P35
ACID靠什么保证的
06:46
P36
什么是MVCC
10:58
P37
mysql主从同步原理
06:17
P38
简述Myisam和Innodb的区别
05:23
P39
简述mysql中索引类型及对数据库的性能的影响
06:41
P40
MySQL有哪几种数据存储引擎
12:09
P41
什么是脏读、幻读、不可重复读
10:26
P42
事务的基本特性和隔离级别
10:02
P43
MySQL的锁有哪些
13:40
P44
MySQL的索引结构是什么样的
19:43
P45
MySQL集群如何搭建
13:36
P46
谈谈如何对MySQL进行分库分表
24:01
P47
什么是倒排索引
14:18
P48
Mysql数据库中，什么情况下设置了索引但无法使用
02:07
P49
B树和B+树的区别，为什么Mysql使用B+树
04:32
P50
Mysql锁有哪些，如何理解
02:40
P51
Mysql慢查询该如何优化？
