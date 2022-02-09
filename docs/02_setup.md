# 環境構築
## インストール
各種OS以下コマンドでインストールする事ができます。  

CentOS 7  
`sudo yum -y install git`  

CentOS 8  
`sudo dnf -y install git`  

Ubuntu  
`sudo apt install git`  

alpine  
`sudo apk add git`  

Windows
`winget install --id Git.Git`  

## Githubアカウントの作成
既にアカウント作成済みの場合は読み飛ばして貰って構いません。

[github.com](https://github.com)にアクセスしてsign upしてください。  
画面にそって入力すれば作成できるかと思います。  
ユーザー名は既存のユーザーと同じものは使えないので怒られたら変えてください。

## 初期設定
GitクライアントにGithubのアカウント情報を教えてあげる必要があるので以下コマンドを用いて設定します。  
メールアドレスは公開しても問題のないアドレスを使用してください。後々公開状態になる可能性があります。  

本稿ではLinuxはbash, WindowsはGit Bashを用いて操作することを前提にコマンドを記述しています。  

Windows標準のコマンドプロンプトからでも実行は可能ですがUnix系とコマンドが違うため、Windows独自コマンドを覚えるように汎用性が高いです。  
要するにWindowsくそってことです。  

```
git config --global user.name "Githubアカウントのユーザー名"
git config --global user.email "メールアドレス"
```  

Gitでは様々な設定をgit configコマンドを用いて行います。  
後々説明する為詳しくは割愛しますが、globalオプションを付加することで、作業しているユーザー全体で適用されます。  

## SSH Keyの設定


`ssh-keygen`  

[目次へ](../README.md)
