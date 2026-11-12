---
layout: default
title: Tips
nav_order: 1
---

# Tips

### 1.VIM

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

**vim.xlam**


| Type | Keystroke | Action | Description | Count |
| ---- | --------- | ------ | ----------- | ----- |
| Core | `<C-m>` | `ToggleVim` | Toggle Vim mode | |
| Moving | `gg` | `MoveToTopRow` | Move to the 1st row or the `[count]`-th row | ✓ |
| Cell | `FF`/`Ff` | `ApplyFlashFill` | Flash Fill (fallback to Auto Fill if not applicable) | |
| Mode | `v` | `ToggleVisualMode` | Toggle visual mode (extend selection) | |
| Border | `bb` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, thin line) | |
| Border | `ba` | `ToggleBorderAround` | Set borders around the selected cells (solid, thin line) | |
| Border | `bia` | `ToggleBorderInner` | Set borders inside the selected cells (solid, thin line) | |
| Row | `ra` | `AppendRows` | Insert rows below the current row | ✓ |
| Row | `ri` | `InsertRows` | Insert rows above the current row | ✓ |
| Row | `rd` | `DeleteRows` | Delete the current row | ✓ |
| Column | `ca` | `AppendColumns` | Insert columns to the right of the current column | ✓ |
| Column | `ci` | `InsertColumns` | Insert columns to the left of the current column | ✓ |
| Column | `cd` | `DeleteColumns` | Delete the current column | ✓ |
| Delete | `D`/`X` | `DeleteValue` | Delete the value in the cell | |
| Paste | `p` | `PasteSmart` | Paste after copying rows or columns; otherwise, send `Ctrl + V` | ✓ |
| Paste | `P` | `PasteSmart` | Paste before copying rows or columns; otherwise, send `Ctrl + V` | ✓ |
| Font | `-` | `DecreaseFontSize` | Decrease font size | ✓ |
| Font | `+` | `IncreaseFontSize` | Increase font size | ✓ |
| Color | `fc` | `SmartFontColor` | Show the font color selection dialog | |
| Find & Replace | `/` | `ShowFindFollowLang` | Show the find dialog, following the language mode of IME | |
| Find & Replace | `n` | `NextFoundCell` | Select the next found cell | ✓ |
| Find & Replace | `N` | `PreviousFoundCell` | Select the previous found cell | ✓ |
| Scrolling | `<C-u>` | `ScrollUpHalf` | Scroll up by half a page | ✓ |
| Scrolling | `<C-d>` | `ScrollDownHalf` | Scroll down by half a page | ✓ |
| Scrolling | `zt` | `ScrollCurrentTop` | Scroll to make the current row at the top (`SCREEN_OFFSET` pts of padding) | ✓ |
| Scrolling | `zz` | `ScrollCurrentMiddle` | Scroll to make the current row in the middle | ✓ |
| Scrolling | `zb` | `ScrollCurrentBottom` | Scroll to make the current row at the bottom (`SCREEN_OFFSET` pts of padding) | ✓ |
| Sheet | `e` | `NextSheet` | Select the next sheet | ✓ |
| Sheet | `E` | `PreviousSheet` | Select the previous sheet | ✓ |
| Sheet | `ww` | `ShowSheetPicker` | Launch the Sheet Picker | |
| Sheet | `wr` | `RenameSheet` | Change the name of the active sheet | |
| Workbook | `:w` | `SaveWorkbook` | Save the active workbook | |
| Workbook | `:q` | `CloseAskSaving` | Close the active workbook (show a dialog if there are unsaved changes) | |
| Workbook | `:q!`/`ZQ` | `CloseWithoutSaving` | Close the active workbook without saving | |
| Workbook | `:wq`/`:x`/`ZZ` | `CloseWithSaving` | Save and close the active workbook | |
| Other | `u` | `Undo_CtrlZ` | Undo (send `Ctrl + Z`) | |
| Other | `<C-r>` | `RedoExecute` | Redo | |
| Moving | `gg` | `MoveToFirstRow` | Move to the 1st row or the `[count]`-th row | ✓ |
| Moving | `gG` | `MoveToTopRow` | Move to the first row of UsedRange or the `[count]`-th row | ✓ |
| Moving | `G` | `MoveToLastRow` | Move to the last row of UsedRange or the `[count]`-th row | ✓ |
| Moving | `\|` | `MoveToNthColumn` | Move to the `[count]`-th column | ✓ |
| Moving | `0` | `MoveToFirstColumn` | Move to the 1st column | |
| Moving | `^` | `MoveToLeftEnd` | Move to the first column of UsedRange | |
| Moving | `$` | `MoveToRightEnd` | Move to the last column of UsedRange | |
| Moving | `g0` | `MoveToA1` | Move to cell A1 | |
| Moving | `{` | `MoveToTopOfCurrentRegion` | Move to the first row within the CurrentRegion | |
| Moving | `}` | `MoveToBottomOfCurrentRegion` | Move to the last row within the CurrentRegion | |
| Moving | `W[cell]` | `MoveToSpecifiedCell` | Move to the specified `[cell]` | |
| Moving | `:[num]` | `MoveToSpecifiedRow` | Move to the specified `[num]`-th row | |
| Cell | `ga` | `SelectUsedRange` | Select the UsedRange | |
| Cell | `gA` | `SelectAllCells` | Select all cells | |
| Cell | `<C-S-A>` | `AddNumber` | Add the number | ✓ |
| Cell | `<C-S-X>` | `SubtractNumber` | Subtract the number | ✓ |
| Cell | `g<C-A>` | `VisualAddNumber` | Add the number sequentially | ✓ |
| Cell | `g<C-X>` | `VisualSubtractNumber` | Subtract the number sequentially | ✓ |
| Cell | `zw` | `ToggleWrapText` | Toggle cell wrap text | |
| Cell | `&` | `ToggleMergeCells` | Toggle cell merge | |
| Cell | `g/` | `ShowCellPicker` | Launch CellPicker | |
| Cell | `=s` | `AutoSum` | Auto SUM | |
| Cell | `=a` | `AutoAverage` | Auto SUM (average) | |
| Cell | `=c` | `AutoCount` | Auto SUM (count) | |
| Cell | `=m` | `AutoMax` | Auto SUM (maximum) | |
| Cell | `=i` | `AutoMin` | Auto SUM (minimum) | |
| Cell | `==` | `InsertFunction` | Insert function | |
| Border | `bb` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, thin line) | |
| Border | `ba` | `ToggleBorderAround` | Set borders around the selected cells (solid, thin line) | |
| Border | `bh` | `ToggleBorderLeft` | Set left borders of the selected cells (solid, thin line) | |
| Border | `bj` | `ToggleBorderBottom` | Set bottom borders of the selected cells (solid, thin line) | |
| Border | `bk` | `ToggleBorderTop` | Set top borders of the selected cells (solid, thin line) | |
| Border | `bl` | `ToggleBorderRight` | Set right borders of the selected cells (solid, thin line) | |
| Border | `bia` | `ToggleBorderInner` | Set borders inside the selected cells (solid, thin line) | |
| Border | `bis` | `ToggleBorderInnerHorizontal` | Set horizontal borders inside the selected cells (solid, thin line) | |
| Border | `biv` | `ToggleBorderInnerVertical` | Set vertical borders inside the selected cells (solid, thin line) | |
| Border | `b/` | `ToggleBorderDiagonalUp` | Set diagonal up borders in the selected cells (solid, thin line) | |
| Border | `b\` | `ToggleBorderDiagonalDown` | Set diagonal down borders in the selected cells (solid, thin line) | |
| Border | `bB` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, thick line) | |
| Border | `bA` | `ToggleBorderAround` | Set borders around the selected cells (solid, thick line) | |
| Border | `bH` | `ToggleBorderLeft` | Set left borders of the selected cells (solid, thick line) | |
| Border | `bJ` | `ToggleBorderBottom` | Set bottom borders of the selected cells (solid, thick line) | |
| Border | `bK` | `ToggleBorderTop` | Set top borders of the selected cells (solid, thick line) | |
| Border | `bL` | `ToggleBorderRight` | Set right borders of the selected cells (solid, thick line) | |
| Border | `Bb` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, thick line) | |
| Border | `Ba` | `ToggleBorderAround` | Set borders around the selected cells (solid, thick line) | |
| Border | `Bh` | `ToggleBorderLeft` | Set left borders of the selected cells (solid, thick line) | |
| Border | `Bj` | `ToggleBorderBottom` | Set bottom borders of the selected cells (solid, thick line) | |
| Border | `Bk` | `ToggleBorderTop` | Set top borders of the selected cells (solid, thick line) | |
| Border | `Bl` | `ToggleBorderRight` | Set right borders of the selected cells (solid, thick line) | |
| Border | `Bia` | `ToggleBorderInner` | Set borders inside the selected cells (solid, thick line) | |
| Border | `Bis` | `ToggleBorderInnerHorizontal` | Set horizontal borders inside the selected cells (solid, thick line) | |
| Border | `Biv` | `ToggleBorderInnerVertical` | Set vertical borders inside the selected cells (solid, thick line) | |
| Border | `B/` | `ToggleBorderDiagonalUp` | Set diagonal up borders in the selected cells (solid, thick line) | |
| Border | `B\` | `ToggleBorderDiagonalDown` | Set diagonal down borders in the selected cells (solid, thick line) | |
| Border | `bob` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, hairline) | |
| Border | `boa` | `ToggleBorderAround` | Set borders around the selected cells (solid, hairline) | |
| Border | `boh` | `ToggleBorderLeft` | Set left borders of the selected cells (solid, hairline) | |
| Border | `boj` | `ToggleBorderBottom` | Set bottom borders of the selected cells (solid, hairline) | |
| Border | `bok` | `ToggleBorderTop` | Set top borders of the selected cells (solid, hairline) | |
| Border | `bol` | `ToggleBorderRight` | Set right borders of the selected cells (solid, hairline) | |
| Border | `boia` | `ToggleBorderInner` | Set borders inside the selected cells (solid, hairline) | |
| Border | `bois` | `ToggleBorderInnerHorizontal` | Set horizontal borders inside the selected cells (solid, hairline) | |
| Border | `boiv` | `ToggleBorderInnerVertical` | Set vertical borders inside the selected cells (solid, hairline) | |
| Border | `bo/` | `ToggleBorderDiagonalUp` | Set diagonal up borders in the selected cells (solid, hairline) | |
| Border | `bo\` | `ToggleBorderDiagonalDown` | Set diagonal down borders in the selected cells (solid, hairline) | |
| Border | `bmb` | `ToggleBorderAll` | Set borders around and inside the selected cells (solid, medium line) | |
| Border | `bma` | `ToggleBorderAround` | Set borders around the selected cells (solid, medium line) | |
| Border | `bmh` | `ToggleBorderLeft` | Set left borders of the selected cells (solid, medium line) | |
| Border | `bmj` | `ToggleBorderBottom` | Set bottom borders of the selected cells (solid, medium line) | |
| Border | `bmk` | `ToggleBorderTop` | Set top borders of the selected cells (solid, medium line) | |
| Border | `bml` | `ToggleBorderRight` | Set right borders of the selected cells (solid, medium line) | |
| Border | `bmia` | `ToggleBorderInner` | Set borders inside the selected cells (solid, medium line) | |
| Border | `bmis` | `ToggleBorderInnerHorizontal` | Set horizontal borders inside the selected cells (solid, medium line) | |
| Border | `bmiv` | `ToggleBorderInnerVertical` | Set vertical borders inside the selected cells (solid, medium line) | |
| Border | `bm/` | `ToggleBorderDiagonalUp` | Set diagonal up borders in the selected cells (solid, medium line) | |
| Border | `bm\` | `ToggleBorderDiagonalDown` | Set diagonal down borders in the selected cells (solid, medium line) | |
| Border | `btb` | `ToggleBorderAll` | Set borders around and inside the selected cells (double line, thick line) | |
| Border | `bta` | `ToggleBorderAround` | Set borders around the selected cells (double line, thick line) | |
| Border | `bth` | `ToggleBorderLeft` | Set left borders of the selected cells (double line, thick line) | |
| Border | `btj` | `ToggleBorderBottom` | Set bottom borders of the selected cells (double line, thick line) | |
| Border | `btk` | `ToggleBorderTop` | Set top borders of the selected cells (double line, thick line) | |
| Border | `btl` | `ToggleBorderRight` | Set right borders of the selected cells (double line, thick line) | |
| Border | `btia` | `ToggleBorderInner` | Set borders inside the selected cells (double line, thick line) | |
| Border | `btis` | `ToggleBorderInnerHorizontal` | Set horizontal borders inside the selected cells (double line, thick line) | |
| Border | `btiv` | `ToggleBorderInnerVertical` | Set vertical borders inside the selected cells (double line, thick line) | |
| Border | `bt/` | `ToggleBorderDiagonalUp` | Set diagonal up borders in the selected cells (double line, thick line) | |
| Border | `bt\` | `ToggleBorderDiagonalDown` | Set diagonal down borders in the selected cells (double line, thick line) | |
| Border | `bdd` | `DeleteBorderAll` | Delete all borders around and inside the selected cells | |
| Border | `bda` | `DeleteBorderAround` | Delete borders around the selected cells | |
| Border | `bdh` | `DeleteBorderLeft` | Delete left borders of the selected cells | |
| Border | `bdj` | `DeleteBorderBottom` | Delete bottom borders of the selected cells | |
| Border | `bdk` | `DeleteBorderTop` | Delete top borders of the selected cells | |
| Border | `bdl` | `DeleteBorderRight` | Delete right borders of the selected cells | |
| Border | `bdia` | `DeleteBorderInner` | Delete all inner borders of the selected cells | |
| Border | `bdis` | `DeleteBorderInnerHorizontal` | Delete horizontal inner borders of the selected cells | |
| Border | `bdiv` | `DeleteBorderInnerVertical` | Delete vertical inner borders of the selected cells | |
| Border | `bd/` | `DeleteBorderDiagonalUp` | Delete diagonal up borders in the selected cells | |
| Border | `bd\` | `DeleteBorderDiagonalDown` | Delete diagonal down borders in the selected cells | |
| Border | `bcc` | `SetBorderColorAll` | Set the color of all borders around and inside the selected cells | |
| Border | `bca` | `SetBorderColorAround` | Set the color of borders around the selected cells | |
| Border | `bch` | `SetBorderColorLeft` | Set the color of left borders of the selected cells | |
| Border | `bcj` | `SetBorderColorBottom` | Set the color of bottom borders of the selected cells | |
| Border | `bck` | `SetBorderColorTop` | Set the color of top borders of the selected cells | |
| Border | `bcl` | `SetBorderColorRight` | Set the color of right borders of the selected cells | |
| Border | `bcia` | `SetBorderColorInner` | Set the color of all inner borders of the selected cells | |
| Border | `bcis` | `SetBorderColorInnerHorizontal` | Set the color of horizontal inner borders of the selected cells | |
| Border | `bciv` | `SetBorderColorInnerVertical` | Set the color of vertical inner borders of the selected cells | |
| Border | `bc/` | `SetBorderColorDiagonalUp` | Set the color of diagonal up borders in the selected cells | |
| Border | `bc\` | `SetBorderColorDiagonalDown` | Set the color of diagonal down borders in the selected cells | |
| Row | `r-` | `NarrowRowsHeight` | Narrow the height of the row | ✓ |
| Row | `r+` | `WideRowsHeight` | Widen the height of the row | ✓ |
| Row | `rr` | `SelectRows` | Select rows | ✓ |
| Delete | `D`/`X` | `DeleteValue` | Delete the value in the cell | |
| Delete | `dga` | `DeleteUsedRange` | Delete the UsedRange | |
| Delete | `dgA` | `DeleteAllCells` | Delete all cells | |
| Font | `-` | `DecreaseFontSize` | Decrease font size | ✓ |
| Font | `+` | `IncreaseFontSize` | Increase font size | ✓ |
| Font | `fh` | `AlignLeft` | Align left | |
| Font | `fj` | `AlignBottom` | Align bottom | |
| Font | `fk` | `AlignTop` | Align top | |
| Font | `fl` | `AlignRight` | Align right | |
| Font | `fo` | `AlignCenter` | Align center horizontally | |
| Font | `fm` | `AlignMiddle` | Align center vertically | |
| Font | `fb` | `ToggleBold` | Toggle bold | |
| Comment | `Ci`/`Cc` | `EditCellComment` | Edit the cell comment (add if none exists) | |
| Comment | `Ce`/`Cx`/`Cd` | `DeleteCellComment` | Delete the current cell's comment | |
| Comment | `CE`/`CD` | `DeleteCellCommentAll` | Delete all comments on the sheet | |
| Comment | `Ca` | `ToggleCellComment` | Toggle the display of the current cell's comment | |
| Comment | `Cr` | `ShowCellComment` | Show the current cell's comment | |
| Comment | `Cm` | `HideCellComment` | Hide the current cell's comment | |
| Comment | `CA` | `ToggleCellCommentAll` | Toggle the display of all comments | |
| Comment | `CR` | `ShowCellCommentAll` | Show all comments | |
| Comment | `CM` | `HideCellCommentAll` | Hide all comments | |
| Comment | `CH` | `HideCellCommentIndicator` | Hide the current cell's comment indicator | |
| Comment | `Cn` | `NextComment` | Select the next commented cell | ✓ |
| Comment | `Cp` | `PrevComment` | Select the previous commented cell | ✓ |
| Find & Replace | `R` | `ShowReplaceWindow` | Show the find and replace dialog | |
| Find & Replace | `]s` | `NextShape` | Select the next shape | ✓ |
| Find & Replace | `[s` | `PrevShape` | Select the previous shape | ✓ |
| Filter | `qq` | `ToggleAutoFilter` | Toggle AutoFilter | |
| Filter | `qd` | `ClearCurrentColumnFilter` | Clear filter for current column | |
| Filter | `qD` | `ClearAllFilters` | Clear all filters | |
| Filter | `qsa` | `SortAscending` | Sort ascending | |
| Filter | `qsd` | `SortDescending` | Sort descending | |
| Filter | `qsc` | `SortColor` | Sort by color | |
| Sheet | `e`/`wn` | `NextSheet` | Select the next sheet | ✓ |
| Sheet | `E`/`wp` | `PreviousSheet` | Select the previous sheet | ✓ |
| Sheet | `ww`/`ws` | `ShowSheetPicker` | Launch the Sheet Picker | |
| Sheet | `wr` | `RenameSheet` | Change the name of the active sheet | |
| Sheet | `wh` | `MoveSheetBack` | Move the active sheet one position to the front | ✓ |
| Sheet | `wl` | `MoveSheetForward` | Move the active sheet one position to the back | ✓ |
| Sheet | `wi` | `InsertWorksheet` | Insert a new worksheet in front of the active worksheet | |
| Sheet | `wa` | `AppendWorksheet` | Insert a new worksheet after the active worksheet | |
| Sheet | `wd` | `DeleteSheet` | Delete the active sheet | |
| Sheet | `w0` | `ActivateLastSheet` | Select the last sheet | |
| Sheet | `w$` | `ActivateLastSheet` | Select the last sheet | |
| Sheet | `wc` | `ChangeSheetTabColor` | Change the color of the active sheet tab | |
| Sheet | `wy` | `CloneSheet` | Clone the active sheet | |
| Sheet | `we` | `ExportSheet` | Show the move or copy sheet dialog | |
| Sheet | `w[num]` | `ActivateSheet` | Select the sheet at position `[num]` (only 1-9) | |
| Other | `m` | `ZoomIn` | Zoom in by 10% or `[count]`% | ✓ |
| Other | `M` | `ZoomOut` | Zoom out by 10% or `[count]`% | ✓ |
| Other | `%` | `ZoomSpecifiedScale` | Set the zoom level to `[count]`% (digits `1`-`9` correspond to predefined zoom levels) | ✓ |
| Other | `\` | `ShowContextMenu` | Show the context menu | |
| Other | `:unique` | `RemoveDuplicates` | Delete duplicates rows from sheet | |
| Other | `zf` | `ToggleFreezePanes` | Toggle freeze panes on/off | |
| Other | `zp` | `SetPrintArea` | Set the selected cells as the print area | |
| Other | `zP` | `ClearPrintArea` | Clear the print area | |


### 2.Git

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

### 3. UCRT proxy setting
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
***4.PowerShell Proxy Setting***
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
