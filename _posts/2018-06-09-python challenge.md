---
layout:     post
title:      python challenge
subtitle:   立下一个flag，不断学习，不断去超越
date:       2018-06-09
author:     yindahui
header-img: img/post-bg-swift2.jpg
catalog: true
tags:
    - python
---

## challenge 00

题目链接: [http://www.pythonchallenge.com/pc/def/0.html](http://www.pythonchallenge.com/pc/def/0.html)

根据题目，需要计算2的38次方
``` python
print(2**38)

```
``` bash
D:\python学习\学习记录>python challenge01.py
274877906944
```

## challenge 01

题目链接： [http://www.pythonchallenge.com/pc/def/map.html](http://www.pythonchallenge.com/pc/def/map.html)

根据题目，找出映射规律，可以发现是'abcdefghijklmnopqrstuvwxyz'对应'cdefghijklmnopqrstuvwxyzab'

``` python
content = 'g fmnc wms bgblr rpylqjyrc gr zw fylb. rfyrq ufyr amknsrcpq ypc dmp. bmgle gr gl zw fylb gq glcddgagclr ylb rfyr\'q ufw rfgq rcvr gq qm jmle. sqgle qrpgle.kyicrpylq() gq pcamkkclbcb. lmu ynnjw ml rfc spj.'
content = 'map'
origin_content = '' 
for c in content:
    if 97 <= ord(c) <= 120:
        c_ascii = ord(c) + 2
        origin_c = chr(c_ascii)
        origin_content = origin_content + origin_c   
    elif ord(c) == 122:
        origin_content = origin_content + 'b'
    elif ord(c) == 121:
        origin_content = origin_content + 'a'
    else:
        origin_content = origin_content + c  
            
print(origin_content)

``` 

``` bash
D:\python学习\学习记录>python challenge02.py
i hope you didnt translate it by hand. thats what computers are for. doing it in by hand is inefficient and that's why this text is so long. using string.maketrans() is recommended. now apply on the url.
```

根据得出来的这段话，知道了string.maketrans()方法，maketrans() 方法用于创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。

两个字符串的长度必须相同，为一一对应的关系。

```python
content = 'g fmnc wms bgblr rpylqjyrc gr zw fylb. rfyrq ufyr amknsrcpq ypc dmp. bmgle gr gl zw fylb gq glcddgagclr ylb rfyr\'q ufw rfgq rcvr gq qm jmle. sqgle qrpgle.kyicrpylq() gq pcamkkclbcb. lmu ynnjw ml rfc spj.'
trantab = content.maketrans('abcdefghijklmnopqrstuvwxyz', 'cdefghijklmnopqrstuvwxyzab')
print (content.translate(trantab))
```
```bash
D:\python学习\学习记录>python challenge02.py
i hope you didnt translate it by hand. thats what computers are for. doing it in by hand is inefficient and that's why this text is so long. using string.maketrans() is recommended. now apply on the url.
```
第二个使用了方法，简单了很多。第一个是自己经历了从无到有的思考，在男朋友谆谆教导之下实现的，中间还夹杂着不想写，男朋友发火等曲折经历，但是确实有了一些成就感，知道学习不擅长的知识不简单，自己能力也很欠缺，但是坚持就是胜利，希望可以天天进步，战胜自己。在生活上也希望自己越来越有韧劲，变成更好的自己。

