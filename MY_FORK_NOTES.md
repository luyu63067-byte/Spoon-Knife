# 我的第一次 Fork 练习

原项目：<https://github.com/octocat/Spoon-Knife>

这个文件是自己在 Fork 中新增的修改，用来练习分支、提交和推送。

## 两个远程仓库

- `origin`：自己的 Fork，`https://github.com/luyu63067-byte/Spoon-Knife.git`
- `upstream`：原作者仓库，`https://github.com/octocat/Spoon-Knife.git`

## 保存自己的修改

```powershell
git status
git add MY_FORK_NOTES.md
git commit -m "文档：新增 Fork 学习笔记"
git push -u origin codex/first-fork-practice
```

## 同步上游

先提交当前修改，让 `git status` 显示工作区干净，再运行：

```powershell
git switch main
git fetch upstream
git merge --ff-only upstream/main
git push origin main
git switch codex/first-fork-practice
git merge main
```

如果合并提示冲突，暂停并查看报错；不要强制推送覆盖历史。

## Pull Request

自己的分支推送后，可以在 GitHub 的 Compare 页面查看差异。
想提交给原作者时，检查 base 指向原作者仓库，compare 指向自己的分支，填写修改理由再创建 PR。
本练习仅保存到自己的 Fork。
