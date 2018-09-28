电子词典项目，没有做界面，使用前在mysql上建立dict库，在库下建立，user、hist、words共3个列表

user:  id name passwd ...
    mysql> create table user (
        -> id int primary key auto_increment,
        -> name varchar(32) not null,
        -> passwd varchar(16) default '000000');

hist:  id name word time
    mysql> create table hist ( 
        -> id int auto_increment primary key,
        -> name varchar(32) not null,
        -> word varchar(32) not null,
        -> time varchar(64));

words: id word interpret
    mysql> create table words(
        -> id int primary key auto_increment,
        -> word varchar(32) not null,
        -> interpret text not null);
