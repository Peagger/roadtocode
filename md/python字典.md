# Python字典

## bugs

##### 关于 - TypeError: dict.get() takes no keyword arguments

```python
dict.get(key, default=None)
```

此处的关键字传参`default`无需输入,因为python底层调用C实现,default无法解析。