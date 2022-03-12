# マージする
## マージとは
ブランチを統合することをマージと言います。  

`dev`ブランチでの前章の変更を`master`にマージしてみましょう。  

## マージする
まずマージ先のブランチに切り替えます。  
```bash
~/git_learning/ $ git checkout master
```  

`README.md`を確認してみましょう。
```bash
~/git_learning/ $ cat README.md
# github learning
```
`master`ブランチに切り替えたので、`dev`での変更は反映されていません。  

確認出来たらマージしてみましょう。  
マージするには、`git merge`コマンドを用いります。
```bash
~/git_learning/ $ git merge dev
```
マージ出来たら再び`README.md`を確認しましょう。  
```bash
~/git_learning/ $ cat README.md
# github learning
## devでの変更
```



[目次へ](../README.md)
