---
layout:     post                    # 使用的布局（不需要改）
title:      在GFM(Github Favored Markdown)中使用MathJax               # 标题 
date:       2020-10-26              # 时间
author:     twhhome                      # 作者
header-img: img/post-bg-github-cup.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:
	- GFM
	- Latex

---

<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# 方法

在md文件开头加入如下代码：
```
<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>
```

# 效果
This is a math formula written in Latex.  
code:  
```
$ \sigma=\sqrt{\frac{1}{n}{\sum_{k=1}^n(x_i-\bar{x})^2}} $
```
effect:  
$ \sigma=\sqrt{\frac{1}{n}{\sum_{k=1}^n(x_i-\bar{x})^2}} $
