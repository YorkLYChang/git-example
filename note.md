# Git LearningNotes

## 基本觀念
分為Local&Remote，其中Local又分為:
> * working directory
>> 一般工作區域	
> * staging area
>> 暫存區
> * localrepo
>> local檔案庫

## 基本指令
> git --version
>> 查看git版本

> git config 
>> 讀取或設定repository或global opiton
>>> git config --list
>>>> 查看目前設定
>>> git config --global user.name
>>>> 設定使用者名稱
>>> git config --global user.email
>>>> 設定使用者電子信箱

> git init
>> 將所在位置成立git repository

> git status
>> 顯示目前git狀態

> git add <filename>
>> 把檔案加進git staging area

> git diff
>> 比較git working area 與 localrepo之差異

> git commit -m -a [filename] 
>> 把git working area commit到 localrepo
### This is an H3#
> hi
>> hihi

> hihihih
* a
* b
* c
>
+ a
+ b
>
1. Hi
2. HEY
