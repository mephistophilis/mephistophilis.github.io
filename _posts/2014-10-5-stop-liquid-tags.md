---
layout: post
title: 取消文件中Liquid模版tags的转换
---
创建archive.html后，在浏览的时候发现jekyll把我贴进来的代码也当作模版代码解释了。
使用下面的代码就可以停止模版的替换。

```
{{ "{% raw " }}%}
{{ "{% endraw " }}%}
```  


