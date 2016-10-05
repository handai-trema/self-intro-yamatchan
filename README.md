# 自己紹介
大阪府立たんげようちえんの園長先生をやっています．  
gitやRubyは触ったことがないので，この演習がとても楽しみです．  
よろしくお願いします．

# 課題リスト
* 16.10.05
  * [リポジトリ](https://github.com/handai-trema/hello-trema-yamatchan)
  * [report.md](https://github.com/handai-trema/hello-trema-yamatchan/blob/master/report.md)

# 便利なgitコマンド
##リモートリポジトリをローカルリポジトリに取り込む (pull)
    git pull##ブランチを新たに作成する (branch，ブランチを切る)    git branch <branch-name>###ブランチの一覧を確認する    git branch    [出力]    master    *develop-yamada    develop-tange    ※*印は現在のブランチ##ブランチを切り替える (checkout)    git checkout <branch-name>###ブランチを作成し，カレントブランチを新しく作成したブランチにする    git checkout -b <branch-name>↑は以下の2コマンドを集約したもの．覚えていたら，少しだけ楽．    git checkout <branch-name>    git branch <branch-name>##ステージングエリアに編集ファイルを追加する (add)    git add <file-pattern>※``<file-pattern>``は正規表現可能  ※全部のファイルを追加したい場合は以下のコマンドでまとめて追加可能    git add .##ステージングエリアに追加されたファイルをコミットする (commit)    git commit -m "<comment message>"※``-a``オプションをつけると，変更されたファイル(新規ファイルは除く)を検出して，それらを全てコミットできるので，``git add .``を省略できる    git commit -a -m "<commit massage>"※``-m``オプションをつけなければ，コミット時にエディタが立ち上がり，コミットメッセージが複数行で入力できる．    git commit###直前のコミットをやり直す新たな変更を直前のコミットにまとめることができる．  
``add``コマンドで編集したファイルをステージングエリアに追加した後に以下のコマンドを実行    git commit --amendエディタが立ち上がり，コミットメッセージの変更もできる##ローカルリポジトリの変更をリモートリポジトリに反映させる (push)    git push <remote-name> <branch-name>※``<remote-name>``は``remote add``で指定したリモートリポジトリの名前．  
このページの通りに行っていると``origin``になっている．  リモートリポジトリ名は``origin``と名付けるのが慣習である．  ``master``ブランチをプッシュしたい場合は，    git push origin masterとなる．##コミットした場合に変更されるファイルを確認する (status)    git status##コミットのログを確認する (log)    git log※長い場合は途中で``q``を入力すれば，ログ表示を終了できる##ステージングエリアに追加していないファイルの差分を確認する (diff)    git diff###次のコミットで反映される変更を表示    git diff --cachedステージングエリアとHEAD(最新のコミット)の差分を表示コミットの直前によく実行するコマンド##ステージングエリアのファイル・フォルダを削除する (rm)    git rm <file-pattern>

