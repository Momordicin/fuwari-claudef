---  
title: Welcome!  
published: 2026-01-13   
description: "Movie starts."  
image: "./1.jpg"  
tags: ["Self-intro"]  
category: Guides  
pinned: true  
draft: false  
---  
# 自我介绍  
Ciallo ～(∠・ω< )⌒★! 这里是没有天赋的AI工程师一枚, 可以叫我慕雨.  
兴趣是小提琴, b站自学日语中...  
  
在读AI硕士, 目前学研方向是私域AI Agents的应用开发.  
曾经负责B2B企业RAG项目的设计规划和开发工作, 学研期间,  
对RAG系列论文的系统进行过调研学习与复现, 目前在Gitee和Github参与多个开源项目的合作开发.  

目前主要项目是[MintBot](https://github.com/Momordicin/MintBot), 一个集合前后端服务部署, 个性化skill脚本配置, 具有长期记忆能力的AI女友!
  
# 项目  
## MintBot  
### 项目介绍
[MintBot](https://github.com/Momordicin/MintBot) 是一个AI角色伴侣应用，支持扮演任意设定的角色（当前阶段专注角色Nikke Mint）. 桌面端为核心开发方向，手机端为辅助入口. 这是一个集合前后端服务部署, 个性化skill脚本配置, Multiagent能力, 和长期记忆能力的AI!
### 前后端服务开发中
...  
### AI模块开发中
- 对话  
    - 角色  
    - 记忆体  
    - 场景  
- 语音转文本  
- 文本转语音  
- 情绪识别  [SER](https://github.com/Momordicin/SER-lab)  
- 场景分割  
    - 基于RAG系统开发完成, 等待场景测试中  
- 知识库驱动  
    - 开发完成, 等待场景测试中  

## Obsidian Markdown  
这是一个[博客帖子自动格式化工具](https://github.com/Momordicin/obsidian2openmd), 实现自动生成style模板, 处理本地图片链接, 超链接等, 支持UI界面的批量设置.   
已实现智能化的任务配置, 可记忆的自动化任务清单, 一键执行.  
  
开发中功能:
- 有序和无序列表  
- 基于github仓库的本地图片链接  
  
## DailyStartup
这是一个[自动化脚本仓库](https://gist.github.com/Momordicin/ca6ee2afb989193d2d42078556b042e9), 汇集了我常用的一键自动化脚本. 

```
# 日常任务
DailyStartup.bat (桌面)  
    └─→ envDailyStart.bat  
            └─→ startup.ps1  
                ├─ [1/5] 网易云音乐 — 启动、打开指定歌单、点击播放、最小化
                ├─ [2/5] Chrome     — 主屏，批量打开学习网址
                ├─ [3/5] Obsidian   — 副屏，打开指定笔记，焦点到首个笔记
                ├─ [4/5] Taix       — 副屏打开 PC使用报告
                └─ [5/5] Folo       — 主屏打开 每日RSS
# 辅助工具: 获取屏幕像素点坐标
mousepos.bat  
    └─→ mousepos.ps1  
# 开发环境启动　
AIenvStart.bat　
    ├─ [1/4] cmd venv cd 开发根目录
    ├─ [2/4] cmd venv cd 开发根目录(方便启动claude code cli)
    └─→ launcher.vbs  
        ├─ [3/4] 打开vscode
        └─ [4/4] 打开Yaak/Postman
CurrentVenvStartup.bat venv快速启动
```