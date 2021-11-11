# Cesloi-CommandAnalisys
一个简易、实用的命令/命令参数解析器

 **该程序不局限于只在Cesloi项目内使用**
 
## 样例展示
```python
>>> from command import *
>>> v = Command(headers=[""], main=["img", [["download", ["-p", AnyStr]], ["upload", [["-u", AnyStr], ["-f", AnyStr]]]]])
>>> v.analysis("img upload -u http://www.baidu.com")
http://www.baidu.com
>>> v.analysis("img upload -f img.png")
img.png
>>> v = Command(headers=["bot"], main=["get"])
>>> print(v.analysis("bot get")
True
>>> v = Command(headers=["bots", "bot"])
>>> v.analysis("bot")
True
>>> v.analysis("sbot")
False

```
