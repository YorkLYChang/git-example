# Git LearningNotes

## 基本觀念
分為Local&Remote，其中Local又分為:
* working directory
> 一般工作區域	
* staging area
> 暫存區
* localrepo
> local檔案庫

## 基本指令

* git --version
> 查看git版本

* git config 
> 讀取或設定repository或global opiton
> 1. git config --list
>> 查看目前設定
> 2. git config --global user.name
>> 設定使用者名稱
> 3. git config --global user.email
>> 設定使用者電子信箱

> 4. git config --global user.username <remote_name>
>> 設定remote使用者名稱

* git init
> 將所在位置成立git repository

* git status
> 顯示目前git狀態

* git add <filename>
> 把檔案加進git staging area

* git diff
> 比較git working directory 與 localrepo之差異

* git commit [-m] [-a] <filename>
> -m 為message -a 為 add
> 把git working directory commit到 localrepo

* git rm --cached <filename>
> 把staging area內檔案刪除

* git reset <pathspec>
> 把localrepo 與 staging area 的檔案都會被還原到<pathspec>，但 working directory 內的檔案不變

* !! git checkout --<filename>
> !! 把檔案從localrepo checkout 到working directory

* git remote <name> <url>
> git 把remote <url> 加到 <name> 這個使用者，讓專案之道<name>是對應到<url>

* git push [-u <local_name> <remote_name> ]
> -u 是代表--set-upstream,設定 upstream 只要成功push 一次，就可以使local branch開始自動追蹤指定的remote branch
> push 是把local repository push 到remote repository

## Branch

* git checkout [-b] <branch>
> -b 為建立,checkout 為切換branch

* 
## Refrence

* https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/
* https://kingofamani.gitbooks.io/git-teach/content/chapter_2/chapter_2reset_file.html
* https://git-scm.com/docs
