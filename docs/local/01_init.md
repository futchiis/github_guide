## リポジトリとは
ファイルの変更履歴を含むバージョン管理に必要になる様々な情報を保持する場所をリポジトリと呼びます。  
ローカルリポジトリは手元のパソコン内に作成するリポジトリのことです。  
後ほど使いますがリモートリポジトリと呼ばれるリポジトリもあり、一般的には複数人で共有することを目的にサーバー上に作られます。  

## Gitで管理するファイルを作成する
### ワークツリーを作成する
ワークツリーはGitで管理したいファイルを配置するディレクトリのことです。  
本稿ではディレクトリは`git_learning`としホームディレクトリ直下に作成します。  
以下コマンドを用いることでディレクトリを作成する事ができます。  

```bash
~/ $ cd ~/
~/ $ mkdir git_learning
```    

### 管理するファイルを作成する
```bash
~/git_learning/ $ echo "# github learning" > README.md
```
上記コマンドで「`# github learning`」が書き込まれたファイル(README.md)を作成することができます。  

## ローカルリポジトリを作成する
`git init`コマンドでローカルリポジトリを作成することができます。  
作業ディレクトリにローカルリポジトリが作成されるため`~/git_learning/`に移動してから実行してください。

```bash
~/git_learning/ $ git init
```

ディレクトリの内容を確認できるコマンドに`ls`コマンドがあります。  
隠しファイルも表示するために`ls -a`を実行すると`.git`ディレクトリが確認できると思います。  
`.git`ディレクトリ内にGitが管理するデータが含まれるので削除しないよう気をつけてください。

## ローカルリポジトリの状態を確認する
`git status`コマンドを用いることでローカルリポジトリの状態を確認することができます。  
以下が`git status`の実行結果です。  
```
~/git_learning/ $ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```

### git statusの見方
`On branch master`  
masterブランチで作業していることを表します。ブランチについては、後ほど解説するので詳しくは割愛します。  
`No commits yet`  
一度もコミットしてない場合に表示されます。  
`Untracked files:`  
一度も管理対象になってないファイルを表示しています。  
