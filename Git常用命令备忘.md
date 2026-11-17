# Git 常用命令备忘

> 新手只需要记住前 5 条，其余用到再查。

## 一、日常三步（80% 的时间只用这三条）

```bash
git status              # 看现在有什么改动（最常用，不确定就敲它）
git add .               # 把改动放进"待提交区"
git commit -m "说明"    # 存一个版本快照
```

## 二、和 GitHub 同步

```bash
git push                # 本地 → GitHub（上传）
git pull                # GitHub → 本地（下载别人的更新）
git clone <仓库地址>    # 第一次把远端仓库拉到本地
```

## 三、看历史 / 后悔药

```bash
git log --oneline       # 一行一条，看提交历史
git diff                # 看还没 add 的改动内容
git restore <文件名>    # 撤销工作区改动（危险，会丢改动）
git reset HEAD <文件名> # 把文件移出待提交区，改动保留
```

## 四、分支（等熟悉了再碰）

```bash
git switch -c 新分支名  # 新建并切换分支
git switch main         # 切回主分支
git branch              # 看本地分支
git merge 分支名        # 把某分支合并进当前分支
```

## 五、配置（只做一次）

```bash
git config --global user.name "名字"
git config --global user.email "邮箱"
git config --global --list     # 检查配置
ssh -T git@github.com          # 测试 SSH 是否连通
```

## 注意

- 提交说明（-m 后面那串）写清楚"改了什么"，将来自己看得懂，半年后你会感谢自己。
- 别把密码、身份证、API 密钥提交上去。一旦 push 到公开仓库，删掉也会留在历史里。
- `git push` 报 `rejected` 一般是 GitHub 上有你没有的提交，先 `git pull` 再推。
