# git勉強会のハンズオンのア
1. git init
2. git add .
3. git commit -m 'fuck'
4. git remote add origin fuck.com
5. git push origin master
6. git checkout -b 'fucking_branch'
7. なんかやって2〜3を再びやる
8. git checkout master 
9. git merge fucking_branch
10. git clone fuck.com


# ハンズオン資料
この資料にそって、実際にコマンドを打ち込んで学習していきます。

1. 準備
まず初めに、適当な場所にgit勉強会用のフォルダ(git_studyなど)を作って、HTMLファイルを作成してください。
[勉強用HTML](https://github.com/gn-spawn/git-study/blob/master/index.html)から作成したHTMLにコピペしてください。

2. gitの設定
```git config --global user.name "あなたの名前"```
```git config --global user.email "メールアドレス"```


3. gitを使ってみる
```git init ```
を実行します。これを実行すると、gitオブジェクトが作成され、gitコマンドを使えるようになります。このコマンドはプロジェクトで作業を始める最初にだけ実行します。
```git add .```
を実行します。```git add```コマンドは、ファイルやフォルダをステージングエリアに移動します。```git add .```は新規作成されたものと、変更があったものをaddします。
```git commit -m 'メッセージ'```
このコマンドでコミットをします。メッセージは履歴で見た時に分かりやすいように、書きます。
ここで、
```git log```を実行して、コミットを確認してみてください。Qキーで終了できます。

4. ブランチとマージ
ここで、ブランチを切ってみましょう。
```git checkout -b 'ブランチの名前'```で新しくブランチを切ることができます。
新しくブランチを作成できたら、```git branch```でブランチを確認してみましょう。masterと新しく作成したブランチが表示されるはずです。

ここでHTMLに何か追記(h2タグを追加するなど)して、```add.```から```commit```まで復習がてらもう一度一通りやってみましょう。
ここで、マージをしてみましょう。マージは他のブランチの変更を統合することです。
いったん、```git checkout master```でmasterブランチに戻ってください。そこで```git merge (ブランチの名前)```をすると、masterブランチに変更がマージされます。

5. リモートリポジトリとプッシュ
ここから、ローカルからGithub上のリモートリポジトリにプロジェクトをアップしてみましょう。
[この記事](http://qiita.com/shizuma/items/2b2f873a0034839e47ce)を参考にGithubにSSHキーの登録を行ってください。
分からない人やは運営に遠慮なく相談してください。

Githubのリポジトリの作成は[ここ](http://d.hatena.ne.jp/yk5656/20140212/1393158928)を参考に作成してください。

リポジトリが作成できたら、コマンドプロンプトに戻り、```git remote add origin リポジトリのURL```を実行してください。
```git push origin master```するとmasterブランチがGithubのリポジトリにアップロードされます




