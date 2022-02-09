# リモートリポジトリを使う
## リモートリポジトリを作成する
リモートリポジトリはコマンドでは作れないので[github.com](https://github.com)にアクセスして作成します。  
![作成ボタンの画像](https://raw.githubusercontent.com/ama-sosei/github_guide/img/create_remote_repo.png)  
このボタンから作成ページにアクセスすることができるので、画面に沿って入力してください。  

### Repository name
リポジトリ名です。  
`A-Za-z`(アルファベット),`0-9`(数字),`-`(ハイフン),`_`(アンダースコア)を使ってください。  
日本語などの2byte文字も使用可能ですが使わないでください。  

### Description
リポジトリの内容についての説明です。  
入力は任意です。  

### Public OR Private
リポジトリを公開するか、非公開にするかの設定です。  
公開時は`Public`を非公開時は`Private`を選択してください。  
非公開設定にしても一部のユーザーにのみ公開することは可能です。  

### Add a README file
リポジトリ作成時に`README.md`を追加する場合はチェックをいれます。  

### Add .gitignore
後ほど解説するので詳しくは割愛しますが`.gitignore`を作成することでコミットを無視するファイルを指定することができます。  
その`.gitignore`をリポジトリ生成時に作成するかの選択です。  

### Choose a license
ライセンスの選択です。  


本稿では以下の設定で作成します。  
```
Repository name: git_learning
Description: 未入力
Public OR Private: Public
Add a README file: no
Add .gitignore: no
Choose a license: 選択なし
```

## リモートリポジトリをローカルリポジトリに紐付ける
`git remote`コマンドを用いり紐付けを行います。  

### コマンド実行例
`git remote add origin リモートリポジトリurl`  

`origin`は別の文字列でも良いですが`origin`を使う風習があるので特別な事情がなければ`origin`を使いましょう。  

### git_learningを紐付ける
先程作ったリモートリポジトリを紐付けします。  

`~/git_learning/ $ git remote add origin git@github.com:githubのユーザー名/git_learning`  

もし今後urlの変更が必要になったら`git remote rm origin`で紐付けを解除することができます。  
リモートリポジトリの削除はしないので必要があれば`https://github.com/ユーザー名/リポジトリ名`の`Setting`から削除する必要があります。  

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


[目次へ](../README.md)
