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

xp                  # 交换两个字符
ddp                 # 交换两行
bi                  # 单词前加入字符
ea                  # 单词后加入字符
[N]r<Enter>         # 用一个换行符替换 N 个字符
g Ctrl+G            # 单词统计，按 g 再同时按 Ctrl+g 组合键
```

**EasyAlign**
```
- vipga*|
- vipga<enter>*|
- vipga<enter><enter>*|

<enter> 选择对接方式：左中（C）右（R），默认左对齐
```

**2.Git**
```
git add .
git commit -m "msg"
git push

git fetch --all && git reset --hard origin/main && git pull
```

输入下面的命令修改远程仓库地址：

`git remote set-url origin git@bitbucket.org:你的用户名/仓库名.git`

可以用这个命令检查是否修改成功：

`git remote -v`

**3. UCRT proxy setting**
```
set:
  export http_proxy  = 127.0.0.1:10808
  export https_proxy = 127.0.0.1:10808

unset:
  export http_proxy
  export https_proxy

test:
  curl cip.cc
 ```
**4.PowerShell Proxy Setting**
步骤 1：找到并编辑 PowerShell 配置文件

首先，我们需要找到 PowerShell 的配置文件。如果你还没有创建过，可以用以下命令创建：
```
if (!(Test-Path -Path $PROFILE)) {
    New-Item -ItemType File -Path $PROFILE -Force
}
notepad $PROFILE
```
这会打开你的 PowerShell 配置文件。配置文件的默认路径通常是： C:\Users\你的用户名\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
步骤 2：添加代理函数

在打开的配置文件中，添加以下函数：
```
function proxy {
    $env:http_proxy  = "http://127.0.0.1:10809"
    $env:https_proxy = "http://127.0.0.1:10809"
    [System.Net.WebRequest]::DefaultWebProxy = New-Object System.Net.WebProxy("http://127.0.0.1:10809")
    Write-Host "Proxy enabled: http://127.0.0.1:10809" -ForegroundColor Green
}

function unproxy {
    $env:http_proxy  = $null
    $env:https_proxy = $null
    [System.Net.WebRequest]::DefaultWebProxy = $null
    Write-Host "Proxy disabled" -ForegroundColor Yellow
}

function check-proxy {
    if ($env:http_proxy -or $env:https_proxy) {
        Write-Host "Current proxy settings:" -ForegroundColor Cyan
        Write-Host "HTTP Proxy: $env:http_proxy"
        Write-Host "HTTPS Proxy: $env:https_proxy"
    } else {
        Write-Host "No proxy is currently set." -ForegroundColor Cyan
    }
}
```
步骤 3：保存并重新加载配置

保存文件，然后重新启动 PowerShell 或运行 . $PROFILE 来重新加载配置文件。
如何使用

现在，你可以在 PowerShell 中使用以下命令：
```
    输入 proxy 来启用代理
    输入 unproxy 来禁用代理
    输入 check-proxy 来查看当前的代理设置
```

此系统上禁止运行脚本
出现此问题可执行下面命令启用配置，输入Y回车

`Set-ExecutionPolicy RemoteSigned`
