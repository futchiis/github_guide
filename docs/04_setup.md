# setup

## githubアカウントの作成
[github](https://github.com)でsign up  
めんどいから細かいことは省略  

## ローカルでアカウント設定
bashなりcmdなりで以下を実行
```
git config --global user.name "ユーザー名"
git config --global user.email "メアド"
```

## ssh keyの作成と登録
gitとは直接関係ない知識なので説明は割愛します  
以下コマンドで作成  
```
mkdir ~/.ssh
cd ~/.ssh
ssh-keygen -b 4096 -f "~/.ssh/github"
```
パスフレーズは入れずに脳死エンターでもおｋ  

設定ファイルを作成するため以下コマンドでエディタを開く  
Linux -> `nano \~/.ssh/config`  
Windows -> `notepad \~/.ssh/config`  
以下を貼り付けて保存  
```Host github
  HostName github.com
  User git
  IdentityFile ~/.ssh/github
  IdentitiesOnly yes
```


linuxは以下コマンドも実行  
```
chmod 600 ~/.ssh/*
chmod 700 ~/.ssh
```

githubに公開鍵を登録するため以下コマンドで公開鍵を確認する  
Linux -> `cat ~/.ssh/github.pub`  
Windows -> `type ~/.ssh/github.pub`  

表示された文字列をコピーしておく。  

1. 登録するためgithubにアクセスし設定画面を開く
2. `SSH and GPG keys`を選択
3. `New SSH Key`をクリック
4. Titleは自由, keyに公開鍵を貼り付けて`Add SSH key`をクリック
5. 完

ちゃんと登録できたか確認するため以下コマンドを実行する。  
`ssh -T github`  

`Are you sure you want to continue connecting (yes/no/[fingerprint])?`って聞かれたらyesでエンター

以下が返ってきたらおｋ  
`Hi "ユーザー名"! You've successfully authenticated, but GitHub does not provide shell access.`

[目次へ](../README.md)

