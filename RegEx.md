# 正则表达式

> 练习网址：https://regex101.com

## 1.	字符匹配

```python
.  # 匹配任意字符
```

```python
[ ]  # 匹配内部单个字符(字符关系为 or )
```

```python
[^  ]  # 匹配出去括号内的所有字符
```

```python
# 举例
[a-z], [A-Z], [0-9], [a-zA-Z0-9]  # 匹配小写，大写，数字, 前三者之和
```

```python
\d  # 代表所有数字
```

```python
\w  # 代表所有单词字符
```

```python
\s  # 代表所有空白(包括空格符与制表符)
```

## 2.	字段匹配

```python
a*  # 匹配 * 前一字符的n个匹配项目, n∈Z
```

```python
# 举例
ab* --> a, ab, abb, abbb, etc...
```

```python
a+  # 匹配 + 前一字符的n个匹配项目, n∈Z, n≠0
```

```
# 举例
ab+ --> ab, abb, abbb, etc...
```

```python
a?  # 匹配 ? 前一字符的n个匹配项目, n∈[0,1], n∈Z
```

```python
# 举例
ab? --> a, ab
```

```python
a{2,4}  # 匹配两到四个a
```

```python
# 举例(日期)
[30/12/2020:22:25:00 UTC+8] --> \[(\d)+\/(\d+)\/(\d+):(\d+):(\d+):(\d+)\s(\w+\+\d)\]
# 括号内分别对应日, 月, 年, 时, 分, 秒, 时区
```

```python
[30/12/2020:22:25:00 UTC+8] --> \[(\d)+\/(\d+)\/(\d+):(\d+):(\d+):(\d+)\s(\w+\+\d)\]
# 每个括号为一个Group
```

```python
[30/12/2020:22:25:00 UTC+8] --> \[(?p<day>\d)+\/(\d+)\/(\d+):(\d+):(\d+):(\d+)\s(\w+\+\d)\]
# 给group重命名
```

```python
a.*a  # 匹配从a到a(最长)
```

```python
a.*?a  # 匹配从a到a(最短)
```

```python
(a|b|c)  # a or b or c
```

```python
^\s$  # 匹配空白行
```

