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


[目次へ](../README.md)
