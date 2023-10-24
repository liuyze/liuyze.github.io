---
layout: '[post]'
title: python学习笔记
date: 2020-12-22 16:53:35
tags:

---

# python学习笔记==

## 1.判断文件是否存在：

  1）方法一：

```python
import os

os.path.isfile('/xxx/xxx/filename')   #判断文件是否存在

os.path.exists("path")   #判断文件夹是否存在
```

​       判断文件的权限

​      使用`os.access()`方法判断文件是否可进行读写操作。

```python
import os
#文件是否存在
if os.access("/file/path/foo.txt", os.F_OK):
    print "Given file path is exist."
#文件是否可读
if os.access("/file/path/foo.txt", os.R_OK):
    print "File is accessible to read"
#文件是否可写
if os.access("/file/path/foo.txt", os.W_OK):
    print "File is accessible to write"
#文件是否可执行
if os.access("/file/path/foo.txt", os.X_OK):
    print "File is accessible to execute"
```

2）方法二：

```python
try: #当文件不存在时会抛出异常
    f =open("")
    f.close("")
except FileNotFoundError:
    print "File is not found."
except PersmissionError:
    print "You don't have permission to access this file."
```

 3）方法三：

​        通过pathlib模块判断：

```python
#检查路径是否存在
path = pathlib.Path("path/file")
path.exist()
#检查是否是文件
path = pathlib.Path("path/file")
path.is_file()
```



   