# ファイルの差分を確認する
ファイルの修正前と修正後の違いを差分と言います。  
差分を確認するには`git diff`コマンドを使います。  


## 差分を確認するファイルを用意する
`README.md`に変更を加えます。
```bash
~/git_learning/ $ echo "## ここは差分" >> README.md
```

## ステージングエリアとワークツリーの差分を確認する
`git diff`コマンドを実行して差分を確認してみましょう。  

```bash
~/git_learning/ $ git diff
diff --git a/README.md b/README.md
index e03ba55..cc7cd82 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,3 @@
 "# github learning"
 "## devでの変更"
+"## ここは差分"
```  
`+`から始まる行が追記された行です。  

## コミットとワークツリーの差分確認
`git diff <<コミット>>`  
コミットを表すものであればなんでもおｋです。  
例
- HEAD
- master
- dev
- コミットハッシュ

[目次へ](../README.md)


