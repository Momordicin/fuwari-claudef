---  
title: 项目开发Git使用手册  
published: 2026-06-19  
description: Booklist for past few years  
tags: [Github,Git]  
category: Coding  
draft: false  
---  
  
```bash  
# git config   
git config --global user.name  
git config --global user.email  
  
# 0.1 每次开始工作前，只更新 main  
# git init  
  
# git clone git@github.com:Momordicin/xx.git  
# git remote add origin "https://github.com/..."   
# git push --set-upstream origin main  
# 把本地 main 分支推送到远程 origin,同时 --set-upstream(简写 -u)建立"跟踪关系"  
# git clone, or git remote add + git push --set-upstream  
  
git checkout main  
git pull origin main  
  
# 1. 切到你要开发的功能分支，rebase 一下 main  
git checkout refactor/en-comments # git checkout -b refactor/en-comments   
# git branch -M yyy # 当前分支重命名  
# git rebase main  
# rebase 会改写提交历史  
# 在你自己的功能分支上 rebase main 是安全的(让你的分支基于最新的 main)  
# 铁律:已经 push 到远程、且别人可能基于它工作的分支,不要 rebase  
# 单人开发没这个问题,多人协作时要警惕  
  
# 如果是:  
# 改写任务中的注释改写, 就可以命名refactor/en-comments  
# fix/ 修bug   
# exp/wavlm-finetune 实验性代码  
# docs/update-readme 文档更新  
# refactor/en-comments 整理或重构  
# feat/add-wav2vec2 新功能  
  
# 2. 写代码  
git stash # 临时改动暂存并切回main  
git stash pop # 取出临时改动  
git log --oneline --graph # 图形化方式看提交历史和分支走向, 如 排查"这个改动是哪来的"  
  
# 3. 提交  
git status  
git add . --dry-run # check  
git add . # 提交  
git commit -m "docs: your change description" # 增加提交描述  
# feat: 新功能  
# fix: 修bug  
# chore: 杂项  
# docs: 文档  
# refactor: 重构  
  
git rm -r --cached __pycache__   
# 是删除已经被追踪上传过的__pycache__文件夹  
git add .gitignore  
git commit -m ""  
# amend 只用于未 push 的提交  
git commit --amend --no-edit  
git commit --amend -m "feat: add provider" -m "支持 Anthropic 和 Ollama" -m "由配置决定"  
  
  
# 4. 推送到仓库  
git push origin refactor/en-comments --force-with-lease# 和前面的分支名字一致  
# `--force-with-lease` 会先检查远程分支有没有别人的新提  
# 如果有就拒绝推送,避免你覆盖掉别人的工作  
  
# 5. 在github上 -> Compare & pull request/点击New Pull requests选中推送的branch -> 填写描述 → Create pull request  
# 6. 在PR页面 Review → Approve → 等待管理员Squash and merge(免费github只能这样)  
  
# 7. **确认合并后**, 再清理本地分支  
# 切换回 main 分支  
# 拉取最新代码  
# 删除当前分支  
git checkout main   
git pull origin main   
git branch -d refactor/en-comments   
```