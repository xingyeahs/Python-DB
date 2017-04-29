# 练习 {#练习}

#### 创建表 {#创建表}

* 创建科目表subjects
  * id
  * name
  * isdelete

```
create table subjects(
    id int unsigned auto_increment primary key not null,
    name varchar(20),
    isdelete bit default 0
);

```

* 创建成绩表scores
  * id
  * score
  * stuid
  * subid

```
create table scores(
    id int unsigned auto_increment primary key not null,
    score int,
    stuid int unsigned,
    subid int unsigned,
    foreign key(stuid) references students(id),
    foreign key(subid) references subjects(id)
);

```

#### 添加数据 {#添加数据}

* 示例数据，用于查询练习

```
insert into subjects(name) values('python'),('数据库'),('前端');

insert into scores(score,stuid,subid) values(100,1,1),(98,1,2),(90,1,3),(95,2,1),(100,2,2),(98,2,3),(90,3,1),(80,3,2),(85,3,3),(70,4,1),(60,4,2),(87,4,3);
```



