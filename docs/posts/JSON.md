## 存储数据

模块json让你能够将简单的Python数据结构转储到文件中，并在程序再次运行时加载该文件中的数据。你还可以使用json在Python程序之间分享数据。更重要的是，JSON数据格式并非Python专用的，这让你能够将以JSON格式存储的数据与使用其他编程语言的人分享。这是一种轻便格式，很有用，也易于学习。

JSON(JavaScript Object Notation)格式最初是为JavaScript开发的，但随后成了一种常见格式，被包括Python在内的众多语言采用。

### 使用json.dump()和json.load()

1.使用json.dump()来存储数字列表

```PY
import json
numbers = [2,3,5,7,11,13]
filename = 'numbers.json'
with open(filename,'w') as f_obj:
    json.dump(numbers,f_obj)
```

导入模块json,创建一个数字列表,指定存储数字列表的文件名称

（使用文件扩展名.json来指出文件存储的数据为JSON格式）

2.使用json.load()读取

```py
import json
filename = 'numbers.json'
with open(filename) as f_obj:
    numbers = json.load(f_obj)
print(numbers)
```

