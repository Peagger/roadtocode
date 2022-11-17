# Sqlite3数据库

## bugs

##### near "s": syntax error

```python
sql_condition=' AND '.join("{} = '{}'".format(i,j) for i,j in condition.items())
```

 **单引号** 的使用不当导致的

第二个{}用单引号包围,输入的语句里面有单引号导致错误匹配

本质上是sql注入 

解决方式：将输入中的\'replace成''

```python
' AND '.join("{} = '{}'".format(i,str(j).replace('\'','\'\''))
```


