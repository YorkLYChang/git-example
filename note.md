# Git LearningNotes
## 基本觀念

分為Local&Remote，其中Local又分為:
* working directory
  > 一般工作區域	

* staging area
  > 暫存區

* local repository
  > local檔案庫
 
**關係如圖**

![GITHUB]( https://git-scm.com/book/en/v2/images/areas.png "GIT")

## 建立

* git init
  > 將所在位置成立git repository

## 基本指令

* git --version
  > 查看git版本

* git status
  > 顯示目前git狀態

* git diff
  > 比較git working directory 與 local repository之差異

* git add <filename>
  > 把檔案加進git staging area

* git commit [-a] [-m <comment>]
  > -m 為message -a 為 add
  > 把git working directory commit到 repository

* git rm --cached <filename>
  > 把staging area內檔案刪除

* git checkout [pathspec] <file_name>
  >把local repository 名為<file_name>的檔案覆蓋到working directory 內
  >若有[pathspec]參數，則以[pathspec]版本的local repository

* git reset <pathspec>
  > 把local repository 與 staging area 的檔案都還原到<pathspec>版本，但 working directory 內的檔案不變
  > <pathspec> ex:HEAD,HEAD~...
  
## 設定

* git config 
  > 讀取或設定repository或global opiton

* git config --list
  > 查看目前設定

* git config --global user.name
  > 設定使用者名稱

* git config --global user.email
  > 設定使用者電子信箱

* git config --global user.username <remote_name>
  > 設定remote使用者名稱

## Branch

* git branch [-d] [branchname]
  > 如有帶<branchname>參數，建立名字為<branchname>的Branch
  > 如有帶-d 參數，則刪除名字為<branchname>的Branch
  > 如沒帶參數則顯示Branch List及用*在前表示現在所在之Branch

* git checkout <branchname>
  > 切換至名字為<branchname>的branch

* git merge <branchname>adasdas
  > 合併現在所在之Branch及名字為<branchname>之Branch
  > 如有衝突則必須手動修改解決衝突
 
* git rebase [--abort][--continue]<branchname>
  > 更改從哪裡Branthch出來再目前之Branch修改點Merge上去
  > 如有衝突必須手動修改解決衝突後再帶[--continue]繼續執行
  > 如要取消rebase則帶[--abort]
 
## 遠端

* git remote <name> <url>
  > git 把remote <url> 加到 <name> 這個使用者，讓專案之道<name>是對應到<url>

* git clone <url>
  > git 把<url>所在之專案內的檔案複製到local端

* git push [-u <remote_name> <local_name> ]
  > -u 是代表--set-upstream,設定 upstream 只要成功push 一次，就可以使local branch開始自動追蹤指定的remote branch
  > push 是把local repository push 到remote repository

* git pull
  > 把remote repository pull 到 local repository

* git fetch
  > 把remote repository 複製下來放到新的一個Branch

## Tag

* git tag
  > 查看目前有哪些tag

* git tag [-d] <tagname>
  > 在當前得版本加入tag
  > 若有帶[-d]參數，則刪除tag
  
* git tag -am <"輸入註解"> <tagname>
  > 在當前的版本加入tag,並附帶註解
  

## Refrence

* https://blog.techbridge.cc/2018/01/17/learning-programming-and-coding-with-python-git-and-github-tutorial/
* https://kingofamani.gitbooks.io/git-teach/content/chapter_2/chapter_2reset_file.html
* https://git-scm.com/docs
* https://backlog.com/git-tutorial/tw/stepup/stepup3_2.html
