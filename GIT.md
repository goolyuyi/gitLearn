# 极速掌握 git

### git是代码管理工具(SCM/VCS)
* SCM/VCS Like
  * svn
  * mercurial
  * perforce

* 基本概念:
  * 提交(msg,sha1 id)

* 追踪代码的改变
  * 追踪代码的改变
  * 谁改变的
  * 改变的内容

* 回滚/历史版本
  * 恢复到以前的代码,方便找到问题

* diff/比较差异
  * 比较差异

### git是分布式的

* 分布式仓库
  * 可克隆的:各人仓库是完整的
  * 本地化的:各人仓库是独立的
  * 可分支开发的:各人仓库是持有自己的版本

* 合作模式:
  * 克隆/pull->本地开发->push->合并->pull 循环

### 和 github 的关系
* git 是工具(编辑影片),github 是平台(分享影片)

## git结构
仓库<<分支<<提交<<Tag
Working Tree/Stage Area
Tree

## git操作

### 概览 `git --help`

```bash
These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone             Clone a repository into a new directory
   init              Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add               Add file contents to the index
   mv                Move or rename a file, a directory, or a symlink
   restore           Restore working tree files
   rm                Remove files from the working tree and from the index
   sparse-checkout   Initialize and modify the sparse-checkout

examine the history and state (see also: git help revisions)
   bisect            Use binary search to find the commit that introduced a bug
   diff              Show changes between commits, commit and working tree, etc
   grep              Print lines matching a pattern
   log               Show commit logs
   show              Show various types of objects
   status            Show the working tree status

grow, mark and tweak your common history
   branch            List, create, or delete branches
   commit            Record changes to the repository
   merge             Join two or more development histories together
   rebase            Reapply commits on top of another base tip
   reset             Reset current HEAD to the specified state
   switch            Switch branches
   tag               Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch             Download objects and refs from another repository
   pull              Fetch from and integrate with another repository or a local branch
   push              Update remote refs along with associated objects
```
* [glossary](http://shafiul.github.io/gitbook/7_glossary.html)

## 初始化 `git init/clone`
* from github

## 理解 git 的结构
* git log
* HEAD
* commit with SHA-1

## 第一次提交
* git add
* git status
* git commit

## 第二次提交
* git add -A
* git rm
* git mv
* ignore file

## 历史操作
* checkout: [deprecated](https://medium.com/blue-harvest-tech-blog/git-2-23-0-forget-about-checkout-and-switch-to-restore-ac2682b737b3)
* git restore: history won't change
* git reset: history change
* git tag: 标注
* git diff: 比较

## 分支
* git branch 建立
* git switch 切换
* glo/glol 打印

## 合并
* git commit 分支上提交
* git merge
* git rebase
* git fixup/squash
* git cherry-pick

## 合作/Remote
* git remote

* git push
  * force push

* git pull
* git fetch

## 合作模式
pull/clone -> branch -> dev -> merge -> push -> pull -> merge

# git 的最佳实践

## Best Practice
* 差异比较
  * 文本差异 -- 尽可能使用差异器
  * 别提交 binary -- binary 差异

* working tree/tree/index
  * 可 stash change 或第三方工具

* 分支链chain
  * 区分职责

* 尽快提交--在你无法 handle change 时
  * message
  * squash后再 push/单目的 push
  * 别提交无用文件log/generated file

* push
  * freq push 确保分支完全属于你
  * force push 确保分支完全属于你

* fetch/pull
  * 使用不完全属于你的分支时,务必 fetch/pull

## 案例
* 独自开发
* 两人合作开发



# git flow
git flow


---
https://stackoverflow.com/questions/3689838/whats-the-difference-between-head-working-tree-and-index-in-git

https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

---
完整清单包含:

* Git 的最佳实践
  * merge 时,如何更有效的diff?
  * 个人独立开发是否合适使用 git?
  * 太多分支应该怎么管理?
  * 在公司/多人使用 git 时怎么用?
  * 使用 git,每天应该做的第一件事是什么?
  * 如果有很多细碎提交应该怎么办?
  * git 使用的雷区有哪些?

* git submodules
  * 什么是 monorepo?
  * 如何分离工程和建立大型工程?
  * 如何建立自己的 libs 生态?
  * 如果有大量琐碎工程应该怎么办?
  * 多人合作时怎样更有效的分离任务?

* 工程示例
  * 
