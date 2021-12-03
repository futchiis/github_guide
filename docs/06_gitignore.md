# .gitignore
gitではaddしても管理対象に含めないファイルを設定することができその設定ファイルが`.gitignore`です。  

## どんなファイル?
管理対象に含めないファイルと聞いてもピンとこないかもしないので例をいくつかあげます。

```
*.hex
*.bin
*.exe
*.o
```

なんとなくわかったでしょうか？  
こういったビルド済み生成物などが含まれます。  

## 書いてみる
エディタをひらきます。
Linux -> `nano .gitignore`  
Windows -> `notepad .gitignore`  

```
# #で始まる行はコメント
ignore.md

# 拡張子(ignore)全て無視
*.ignore

# ディレクトリ自体を無視
ignore_dir/

# ディレクトリの中身を全部無視
keep/*

# 逆に残すファイル
!keep/.gitkeep
```
これを書き込みます。  

```
mkdir ignore_dir
mkdir keep

echo "" > ignore.md
echo "" > hoge.ignore
echo "" > keep/.gitkeep

git add .
git commmit -a -m "gitignore test"
git push origin master
```
これで確認できるかと思います


実はgithub公式が[サンプル](https://github.com/github/gitignore)を置いてくれてたりもします。
[目次へ](../README.md)

