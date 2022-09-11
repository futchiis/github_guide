
## ローカルリポジトリのコミットをリモートリポジトリにプッシュする
3章で作成したコミットをリモートリポジトリにアップロードします。  
`~/git_learning/ $ git push origin master`  

以下のような実行結果が帰ってこれば成功です。  
```~/git_learning/ $ git push origin master
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (9/9), 707 bytes | 24.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:ユーザー名/git_learning.git
 * [new branch]      master -> master
```  

もしエラー吐いてたらエラー文でググって修正してください。  

