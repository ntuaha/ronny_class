git
===
- 第一步
先讓本機端的master 聯結到遠端的origin 的連結

        git remote add **遠端repsitory在本機branch的名稱** **github上面的聯結**
        git push -u origin **要送到遠端的目前branch**


- create remote branch and add a local branch to track the remote branch

        git push -u origin remote_branch_name
  
- remove remote branch

        git push origin :remote_branch_name
    
- merge branch,在最後留下來的branch 

        git merge 
    
- remove local branch

        git branch -d remove_branch
    
    
    
處理別人的資料基本流程
======================
1. 複製下來

        git clone <remote_address>
2. 建立local 和 remote 對應        
     
        git checkout --track -b local_branch origin/remote_branch 將遠端的 branch checkout 回來並建立一個新的 local branch，加上 --track 表示你之後還要pull、push回去，所以請 Git 記住對應關係。

3. up-to-date local的資料
       
        git pull (<local_branch_name> origin/<remote_branch_name>) 去遠端 fetch 新版並 merge 進 local branch
        
4. 更新遠端資料
        git push 將 local branch 的 commit 紀錄更新到遠端

    
    
