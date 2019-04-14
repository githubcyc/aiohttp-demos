
## install 

* download
  * 选择免安装版zip版：https://www.postgresql.org/download/windows/
  * Version 9.6.12: https://www.enterprisedb.com/download-postgresql-binaries

* init

```
cd bin
initdb.exe -D D:\postgres\pgsql\data -E UTF-8 --locale=chs -U postgres -W 

// start
pg_ctl -D D:\postgres\pgsql\data -l logfile start

// client
D:\postgres\pgsql\pgAdmin 4\bin\pgAdmin4.exe

// 注册为系统服务
pg_ctl register -N PostgreSQL -D D:\postgres\pgsql\data

// cmd
psql -h localhost -U postgres -d <dbname>

> \c dbname
> \l  == show database;
> \dt 列举表，相当于show tables
> \d tblname 查看表结构，相当于desc tblname, show columns from tbname
```

## Refer

* [install pgsql on Windows](https://blog.csdn.net/weixin_42707253/article/details/86063952)
