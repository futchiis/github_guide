# ブランチを使う
## ブランチとは
gitで管理する履歴を枝分かれさせるための機能です。  
同時に複数の作業をする場合、内容ごとに履歴を管理することが望ましいとされています。  
また、アプリケーションのベータ版と安定版などを分けたいときもブランチを活用すれば容易に切り替えることができます。  

## ブランチを作る
ブランチを作るには`git branch`コマンドを使います。  
ここではブランチ名を`dev`とし作成します。  
```bash
~/git_learning/ $ git branch dev
```  

## ブランチ一覧を表示する
ブランチが作成されたことを確認するためにブランチ一覧を表示させます。  
ブランチ一覧はブランチ名を指定せず`git branch`コマンドを実行することで確認できます。  
```bash
~/git_learning/ $ git branch
  dev
* master
```  
先頭にアスタリスク`*`が表示されているのが、今使ってるブランチです。  

## チェックアウトする
ブランチを切り替えることをチェックアウトと言います。  
チェックアウトするには`git checkout`コマンドを用いります。  
```bash
~/git_learning/ $ git checkout dev
```  

チェックアウトできたことを確認するために`git branch`コマンドを実行しましょう。  
このような表示になっていればでおｋです。  
```bash
~/git_learning/ $ git branch
* dev
  master
```

## 作成とチェックアウトを同時に行う
```bash
git branch dev
git checkout dev
```  
この一連の操作は`git checkout -b dev`で行うこともできます。

## devブランチに変更を加える
`README.md`に変更を加えてコミットします。  

```bash
~/git_learning/ $ echo "## devでの変更" >> README.md
~/git_learning/ $ git add README.md
~/git_learning/ $ git commit -m "devブランチで変更"
```  

## リモートリポジトリに変更を反映する
リモートリポジトリにも`dev`ブランチを作成し変更をアップロードします。  
```bash
~/git_learning/ $ git push origin dev
```  
このように第二引数にブランチ名を指定することでリモートリポジトリにも`dev`ブランチを作成することができます。

[目次へ](../README.md)

