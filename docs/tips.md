---
layout: default
title: Tips
nav_order: 1
---

# Tips

**1.VIM**
```
:%s/<C-r><C-w>/{your_new_word}/g
# % takes the search globally.

使用*向前搜索，使用#向后搜索光标下的单词。启动搜索后，可以使用n在相同方向上重复
搜索，或使用N在相反方向上重复搜索。或者再次使用*或#来代替您所使用的单词。

*和#命令基本上启动搜索，就像您使用/\<word\>或?\<word\>一样。因此，可以在/或?搜索
提示符下使用向上箭头键调用这些搜索。
```

**2.Git**
`
git add .
git commit -m "msg"
git push

git fetch --all && git reset --hard origin/main && git pull
`

输入下面的命令修改远程仓库地址：
`git remote set-url origin git@bitbucket.org:你的用户名/仓库名.git`

可以用这个命令检查是否修改成功：
`git remote -v'
