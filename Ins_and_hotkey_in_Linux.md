Useful instructions and hotkeys
==
## Instructions in Linux terminal
|cd /home |进入 '/ home' 目录'  | 
|:--:|:--:|
|cd .. |返回上一级目录   |
|cd ../.. |返回上两级目录|   
|cd 或 cd ~ |进入个人的主目录   |
|cd ~user1 |进入个人的主目录   |
|cd - |返回上次所在的目录   |
|pwd |显示工作路径|
|ls |查看目录中的文件 |  
|ls -F |查看目录中的文件  | 
|ls -l| 显示文件和目录的详细资料 |
|ls -a |显示隐藏文件| 
|ls *[0-9]* |显示包含数字的文件名和目录名 |
| tree | 显示文件和目录由根目录开始的树形结构(1) | 
| lstree | 显示文件和目录由根目录开始的树形结构(2) | 
| mkdir dir1 | 创建一个叫做 'dir1' 的目录' | 
| mkdir dir1 dir2 | 同时创建两个目录 | 
| mkdir -p /tmp/dir1/dir2 | 创建一个目录树 | 
| rm -f file1 | 删除一个叫做 'file1' 的文件' | 
| rmdir dir1 | 删除一个叫做 'dir1' 的目录' | 
| rm -rf dir1 | 删除一个叫做 'dir1' 的目录并同时删除其内容 | 
| rm -rf dir1 dir2 | 同时删除两个目录及它们的内容 | 
| mv dir1 new_dir | 重命名/移动 一个目录 | 
| cp file1 file2|  复制一个文件 | 
| cp dir/* . | 复制一个目录下的所有文件到当前工作目录 | 
| cp -a /tmp/dir1 . | 复制一个目录到当前工作目录 | 
| cp -a dir1 dir2 | 复制一个目录 | 
| ln -s file1 lnk1 | 创建一个指向文件或目录的软链接 | 
| ln file1 lnk1 | 创建一个指向文件或目录的物理链接 | 
| touch -t 0712250000 file1 | 修改一个文件或目录的时间戳 - (YYMMDDhhmm) | 
| file file1 outputs the mime type of the file as text 
iconv -l |  列出已知的编码 |  

## Hotkey in Linux
1. 启动/寻找程序  
ALT+ F1：启动程序菜单  
ALT+ F2：启动“运行应用程序”对话框

2. 启动终端  
默认是 CTRL + ALT + T, 可以自己调整

3. 窗口切换  
SUPER(WIN) + TAB 和 ALT + TAB 都可以做窗口切换，SUPER + TAB 效果更好，ALT + TAB 更通用。

4. 单个桌面排列窗口  
SUPER + W （SUPER + A）

5. 查看所有工作区的窗口  
通过 SUPER + E 统揽所有工作区所有窗口的运行情况。

6. 移动到新的工作区  
CTRL + SHIFT + 方向键 把这个窗口移到新的工作区中。

7. 移动窗口  
CTRL + ALT + 方向键 帮你在不同的窗口之间进行切换， 你只要记得你要的窗口在哪个工作区，通过这个快捷键就可以到达，当然，你可以直达，为每一个工作区设定一个独立的快捷键。 系统默认允许你为12个工作区设定快捷键。

8. 清空屏幕快捷键  ctrl + l  

9. 清空当前输入快捷键 ctrl + u  

10. 窗口移动模式  
我首先希望通过快捷键让这个窗口在屏幕上移动（这里我的测试硬件是带触摸板的笔记本电脑），我可以通过 点击 ALT + F7 让窗口进入移动模式，然后滑动触摸板，这样我的窗口就会按照我希望的轨迹移动。
 
11. 窗口最大化  
然后是窗口最大化，使用 ALT + F10 ， 这是一个开关，控制我的窗口是最大化还是默认大小。
 
12. 缩小放大屏幕　  
gnome 还允许你放大/缩小你的屏幕，默认没有设置快捷键，我设置的是 CTRL + '+' 来放大，CTRL + ‘-’ 来缩小，然后可以通过触摸板快速移动。
 
13. 清空桌面  
ALT + CTRL + D 迅速将当前工作区的所有窗口最小化，ok，你可以在这个暂时清空的工作区中想想接下来继续做什么。

14. 窗口反色  
super(微软键) + N = 窗口反色  
 
15. 快速锁定屏幕
 
Ctrl + Alt + L
 
16. 鼠标右击的键盘快捷键
 
Shift + F10。
 
17. 重启会话以从崩溃中恢复
 
ubuntu很少会完全崩溃。但如果它真的崩溃了，你可以按下Ctrl + Alt + Backspace来重启会话，恢复的可能达90%。
 
 18. 快速翻页
shift + PgUp 向上翻
shift + PgDn 向下翻

16显示隐藏的文件
 
大多数情况下，你不需要在你的“家“目录中看到那些隐藏文件，但如果你有这个需要，你可以在 Nautilus（ubuntu的文件管理器）下按Ctrl + H来显示隐藏文件。
 
17显示文件属性
 
想要查看文件/文件夹的一般做法是右击选择属性。现在你可以按下 Alt + Enter就能显示属性窗口了
 
 
18反向切换窗口
 
Alt + Tab是切换窗口的快捷键。如果你再按下SHIft，你就可以反向切换窗口。这个快捷键很有用，当你Alt + Tab按得太快，错过了你想要切换的窗口，按一下shift就可以返回之前的窗口了。
 
19显示桌面
 
Ctrl + Alt + D快捷键让你很快地最小化所有窗口，看到桌面。当所有窗口都最小化后，你再按这个快捷键就可以恢复窗口原来的状态。
 
20快速锁定屏幕
 
如果你需要离开电脑一会儿，可以按下Ctrl + Alt + L很快地锁定屏幕，以防有人使用
 
21总结
windows 鍵配合
win + E 在桌面間選擇切換
win + W 在當前桌面的所有窗口間選擇切換
win + A 在所有桌面的所有窗口間選擇切換
win + N 當前窗口反色
win + S 下拉關機菜單
win + M 下拉通信菜單
 
ctrl + alt 鍵配合
ctrl + alt + ← 切換到左邊的桌面
ctrl + alt + → 切換到右邊的桌面
ctrl + alt + shift + ← 移動當前窗口到左邊的桌面
ctrl + alt + shift + → 移動當前窗口到右邊的桌面
ctrl + alt + D 顯示桌面/還原顯示
ctrl + alt + T 啟動終端
ctrl + alt + L 鎖屏/顯示登錄對話框
ctrl + alt + F1-F6 進入1-6命令行環境
ctrl + alt + F7 進入圖形界面環境
 
alt + tab 鍵配合
alt + Tab 在當前桌面的窗口間順序切換
alt + shift + Tab 在當前桌面的窗口間逆序切換
alt + ctrl + Tab 在所有桌面的窗口間順序切換
alt + ctrl + shift + Tab 在所有桌面的窗口間逆序切換
 
other
printscreen 抓圖-全屏
alt + printscreen 抓圖-當前窗口
alt + F10 最大化/取消最大化窗口
alt + F9 最小化窗口
alt + F1 下拉應用程序菜單
alt + F2 打開運行應用程序的窗口
 
終端快捷鍵 
編輯:
複製: ctrl + shift + c
粘貼: ctrl + shift + v
 
窗口:
啟動終端: ctrl + alt + t
新建窗口: ctrl + shift + n
新建標籤: ctrl + shift + t
切換到第i個標籤: alt + i
關閉當前標籤: ctrl + shift + w
關閉窗口: ctrl + shift + q
 
頁面控制
放大: ctrl + + (對於筆記本默認沒有+,則使用ctrl + shift + +)
縮小: ctrl + -
原始大小: ctrl + 0
清理: ctrl + L
全屏: F11
 
配置快捷鍵:
編輯-> 鍵盤快捷鍵
 
gedit 快捷鍵
ctrl + N 新建標籤
ctrl + W 關閉當前標籤
ctrl + Q 關閉整個gedit
ctrl + I 跳轉到行
ctrl + D 刪除當前行或選中的多行
ctrl + F 查找
ctrl + H 替換
ctrl + K 全文高亮匹配查找
alt +上箭頭 向上移動當前行或選中的多行
alt +下箭頭 向下移動當前行或選中的多行

## Hotkey in VsCode

1. 注释：  
a) 单行注释：[ctrl+k,ctrl+c] 或 ctrl+/  
b) 取消单行注释：[ctrl+k,ctrl+u] (按下ctrl不放，再按k + u)  
c) 多行注释：[alt+shift+A]  
d) 多行注释

2. 移动行：alt+up/down


3. 显示/隐藏左侧目录栏 ctrl + b


4. 复制当前行：shift + alt +up/down


5. 删除当前行：shift + ctrl + k

6. 控制台终端显示与隐藏：ctrl + ~

7. 查找文件/安装vs code 插件地址：ctrl + p

8. 代码格式化：shift + alt +f

9. 新建一个窗口: ctrl + shift + n

10. 行增加缩进: ctrl + [

11. 行减少缩进: ctrl + ]

12. 裁剪尾随空格(去掉一行的末尾那些没用的空格) : ctrl + shift + x

13. 字体放大/缩小: ctrl + ( + 或 - )

14. 拆分编辑器 :ctrl + 1/2/3  

15. 切换窗口:  ctrl + shift + left/right  

16. 关闭编辑器窗口:  ctrl + w  

17. 关闭所有窗口 : ctrl + k + w  

18. 切换全屏 :F11  

19. 自动换行:  alt + z  

20. 显示git:   ctrl + shift + g  

21. 全局查找文件：ctrl + p  

22. 显示相关插件的命令(如：git log)：ctrl + shift + p  

23. 选中文字：shift + left / right / up / down  

24. 折叠代码： ctrl + k + 0-9 (0是完全折叠) 
 
25. 展开代码： ctrl + k + j (完全展开代码)  

26. 删除行 ： ctrl + shift + k  

27. 快速切换主题：ctrl + k / ctrl + t  

28. 快速回到顶部 ： ctrl + home  

29. 快速回到底部 : ctrl + end  

30. 格式化选定代码 ：ctrl + k / ctrl +f  

31. 选中代码 ： shift + 鼠标左键  

32. 多行同时添加内容（光标） ：ctrl + alt + up/down 
 
33. 全局替换：ctrl + shift + h  

34. 当前文件替换：ctrl + h  

35. 打开最近打开的文件：ctrl + r  

36. 打开新的命令窗：ctrl + shift + c