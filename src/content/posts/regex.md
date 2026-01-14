---
title: 文本正则记录
published: 2026-01-13 
description: "自存--中文零售文本正则处理SOP"
tags: ["Blogging", "Regex", "Python"]
category: Data Science
draft: false
---

# re 文本正则
## 核心符号
\b: beginning & end  
\w: 字母数字或下划线  
\s: space, tabs, newline  
@: @  
\d : 数字
[A-Z]  [\^A-Z] : 大写字母  非大写字母
[a-z] : 小写字母  
\. : dot  
\^ : 开头
\$ : 结尾
## 核心组合符号
[ ] : 一组字符任一  
*: 0\~n个…  
+: 1\~n个…  
\?: 0\~1个…  
^: 非  
| : 或  
[]{2,}: 2~n个
## 正则经验
复杂业务下, 正则改动往往**牵一发而动全身**: 
1. 正则是上游, 尽早改动和确定
2. 复杂场景分层解决
3. 严格控制上游输出规范]
4. 为下游提供接口和用例文档

Summary: Regex可控性较强, 效率高开销较低, 但是很难更新, 每轮小改动要做全量测试. 
