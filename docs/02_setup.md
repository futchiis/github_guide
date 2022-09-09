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
詳しくは割愛しますが、globalオプションを付加することで、作業しているユーザー全体で適用されます。  

## 公開鍵の設定
gitクライアントから公開鍵暗号方式を用いて認証するために必要な設定を行います。  

<details>
<summary>公開鍵暗号方式とは</summary>

暗号化方式の一つでこのような特徴があります。
- 暗号化と復号化に別々の鍵を使う。
- 暗号化に使う鍵(公開鍵)が公開できる。
- 公開鍵から復号化する鍵(秘密鍵)は数学的に生成不可。
</details>  

### 公開鍵生成
公開鍵暗号方式に必要な公開鍵を生成します。  
`ssh-keygen -t rsa -b 8192`  
生成場所やパスフレーズを聞かれますが脳死でエンター押しても問題ありません。  
既に生成されてる場合上書きされるので気をつけてください。  

公開鍵は`~/.ssh/id_rsa.pub`に生成されてるので中身をコピーしてください。  

githubに公開鍵を登録するために[github.com/settings/ssh/new](https://github.com/settings/ssh/new)にアクセスします。  

`Title`は適当に入力して`Key`に先程コピーした公開鍵をペーストしてください。  
最後に`Add SSH Key`を押せば登録完了です。  

正しく設定できたことを確認するために`ssh -T git@github.com`を実行してください。  

以下が返ってきたらおkです。  

`Hi ユーザー名! You've successfully authenticated, but GitHub does not provide shell access.`




[目次へ](../README.md)
