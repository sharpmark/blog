---
title: 'WWWDOT &#8211; GOOGLE = DOTCOM 解法'
author: sharpmark
layout: post
permalink: /blog/posts/wwwdot-subtrack-google-equal-dotcom-solution/
blogger_blog:
  - sharpmark.blogspot.com
blogger_author:
  - Sharp Mark
blogger_permalink:
  - /2007/04/wwwdot-google-dotcom-solution.html
categories:
  - 挨踢程序产品猿
---
今天无意在网上看到了<a href="http://bbs.yo2.cn/google-ability-tendency-test" target="_blank">Google实验室能力倾向测试</a>  
虽然已经过时了，不过还是很有趣，用了几分钟把第一题作出来了。在这里跟大家分享一下解题过程。原题目如下：

> Solve this cryptic equation, realizing of  
> course that values for M and E could be  
> interchanged. No leading zeros are allowed.  
> WWWDOT &#8211; GOOGLE = DOTCOM

我的解法如下：

<!--more-->

  
先把式子写成竖式方便推算：

<table>
  <tr>
    <td>
      w
    </td>
    
    <td>
      w
    </td>
    
    <td>
      w
    </td>
    
    <td>
      d
    </td>
    
    <td>
      o
    </td>
    
    <td>
      t
    </td>
  </tr>
  
  <tr>
    <td>
      g
    </td>
    
    <td>
      o
    </td>
    
    <td>
      o
    </td>
    
    <td>
      g
    </td>
    
    <td>
      l
    </td>
    
    <td>
      e
    </td>
  </tr>
  
  <tr>
    <td>
      d
    </td>
    
    <td>
      o
    </td>
    
    <td>
      t
    </td>
    
    <td>
      c
    </td>
    
    <td>
      o
    </td>
    
    <td>
      m
    </td>
  </tr>
</table>

观察发现w-o=o, w-o=t。同样的减数，被减数做差不同，只能是产生了借位。(-1都表示低位做运算的时候有借位情况，+10则表示被减数小于减数，导致向高位借位。)  
情况一：  
w &#8211; o = t; w + 10 &#8211; o = o;  
不成立。因为被减的都是o，不可能出现一个借位了，一个没有借。

情况二：  
w &#8211; 1 + 10 &#8211; o = t; (被d &#8211; g借了一位)  
w &#8211; 1 + 10 &#8211; o = o;(上一式成立的前提就是w-1 两等式左边相同，而结果不同，矛盾。

情况三：  
w + 10 &#8211; o = t;  
w + 10 &#8211; 1 &#8211; o = o;(-1是因为上式借位)  
可推出w = 20 &#8211; 9; t = o + 1;  
其中 0 =当o = 5或o = 6时w = 1,或2。w &#8211; g = d中g,d无法取值。  
当o = 7的时候w = 5 t = 8。  
因为w + 10 &#8211; o = t可知其低位d-g=c没有发生借位，即d>g。  
又因为w = 5;所以g = 1, d = 3。(之前有借位)  
当t = 8时，m,e可取值对为(1,7; 2,6; 3,5)。  
当g = 1, d = 3时。c = d &#8211; g = 2;m, e的三对取值都与前假设矛盾。

所以，o = 8。可算出w = 7; t = 9;  
此时d + g = w &#8211; 1 = 6。所以d,g=5,1 或d,g = 4,2。  
当d=4,g=2的时候，c=d-g=2。矛盾。所以d=5,g=1,推出c=4。  
e,m则等于3, 6。o-l=o。所以l=0。  
最后结果：0=l, 1=g, 2没有, 3=m/e, 4=c, 5=d, 6=e/m, 7=w, 8=o, 9=t

之后在网上找到了[另外一种解法][1]。  
第二题以前在校内网讨论过，这里就不多说了。有兴趣的google一下。

 [1]: http://wizard-kevid.spaces.live.com/blog/cns%21bcbb9810a3fed698%211570.entry#trackback