# MySQL数据备份/恢复

## 一、数据备份

### 1.1 使用mysqldump命令备份

mysqldump命令将数据库中的数据备份成一个文本文件。表的结构和表中的数据将存储在生成的文本文件中

```
mysqldump -u username -p dbname table1 table2 ...-> BackupName.sql
示例：备份所有数据库（mysqldump -u username -p -all-databases > BackupName.sql）
```

原理:

```
mysqldump命令的工作原理很简单。它先查出需要备份的表的结构，再在文本文件中生成一个CREATE语句。然后，将表中的所有记录转换成一条INSERT语句。然后通过这些语句，就能够创建表并插入数据。
```

### 1.2 直接复制整个数据库目录

MySQL有一种非常简单的备份方法，就是将MySQL中的数据库文件直接复制出来。这是最简单，速度最快的方法。

PS：注意：这种方法不适用于InnoDB存储引擎的表，而对于MyISAM存储引擎的表很方便。同时，还原时MySQL的版本最好相同。

### 1.3 使用mysqlhotcopy工具快速备份

一看名字就知道是热备份。因此,mysqlhotcopy支持不停止MySQL服务器备份。而且，mysqlhotcopy的备份方式比mysqldump快。mysqlhotcopy是一个perl脚本，主要在Linux系统下使用。其使用LOCK TABLES、FLUSH TABLES和cp来进行快速备份。

```
mysqlhotcopy [option] dbname1 dbname2 backupDir/

backupDir：备份到哪个文件夹下
```

原理：

```
先将需要备份的数据库加上一个读锁，然后用FLUSH TABLES将内存中的数据写回到硬盘上的数据库，最后，把需要备份的数据库文件复制到目标目录

	mysqlhotcopy并非mysql自带，需要安装Perl的数据库接口包
	目前，该工具也仅仅能够备份MyISAM类型的表。
```

## 二、数据还原

### 2.1 还原使用mysqldump命令备份的数据库

*mysql -u root -p [dbname] < backup.sq*

### 2.2 还原直接复制目录的备份

通过这种方式还原时，必须保证两个MySQL数据库的版本号是相同的。MyISAM类型的表有效，对于InnoDB类型的表不可用，InnoDB表的表空间不能直接复制。