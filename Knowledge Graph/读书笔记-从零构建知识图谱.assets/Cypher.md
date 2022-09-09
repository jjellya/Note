# Neo4j - CQL 简介

## 1. 常用命令

| CQL命令  | 用法                         |
| -------- | ---------------------------- |
| CREATE   | 创建结点，关系和属性         |
| MATCH    | 检索有关结点，关系和属性数据 |
| RETURN   | 返回查询结果                 |
| WHERE    | 提供条件过滤检索数据         |
| DELETE   | 删除结点和关系               |
| REMOVE   | 删除结点和关系的属性         |
| ORDER BY | 排序检索数据                 |
| SET      | 添加或更新标签               |



## 2.导入csv文件

#### LOAD载入CSV文件

##### 1、找到安装时设置的数据库所在位置的import文件夹

我的是：D:\Environment\neo4j-chs-community-4.2.2-windows\import

##### 2、从import里面的内容名开始写即可

比如：在import路径下再创建**neo4jResource**目录，将要导入的**csv**文件放到里面：

##### 3、从import里面的内容名开始写即可

比如：在import路径下再创建**neo4jResource**目录，将要导入的**csv**文件放到里面：

在Sell窗口中发送命令：

**对于含有列名的数据：**

```CQL
LOAD CSV WITH HEADERS FROM "file:///neo4jResource/star_nodes_utf8.csv" AS line
create (:star {name:line.name, id:line.id})
```

**对于没有列名的数据：**

```CQL
LOAD CSV WITH HEADERS FROM "file:///neo4jResource/star_nodes_utf8.csv" AS line
create (:star {name:line[0], id:line[1]})
```

**注意：.csv文件要用“记事本”打开，然后点击"另存为"，将格式改成"UTF-8"再进行导入。**



