# Cesloi-CommandAnalisys
一个简易、实用的命令/命令参数解析器
## 样例展示
```python
>>> from command import *
>>> v = Command(headers=[""], main=["img", [["download", ["-p", AnyStr]], ["upload", [["-u", AnyStr], ["-f", AnyStr]]]]])
>>> CommandHandle.analysis_command(v, "img upload -u http://www.baidu.com")
http://www.baidu.com
>>> CommandHandle.analysis_command(v, "img upload -f img.png")
img.png
>>> v = Command(headers=["bot"], main=["get"])
>>> print(CommandHandle.analysis_command(v, "bot get")
True
>>> v = Command(headers=["bots", "bot"])
>>> CommandHandle.analysis_command(v, "bot")
True
>>> CommandHandle.analysis_command(v, "sbot")
False

```
