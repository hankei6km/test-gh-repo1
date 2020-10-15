## Github cli を試すリポジトリ


とりあえず作成してみる。

## gh repo create

`$ gh repo create -d 'Github cli を試すリポジトリ'` を実行し、github 上にリポジトリが作成される。

リモートは以下の通りに設定される。
```
$ git remote -v
origin  git@github.com:hankei6km/test-gh-repo1.git (fetch)
origin  git@github.com:hankei6km/test-gh-repo1.git (push)
```

コマンドを実行した時点では、github 上のリポジトリは空。
`master(main)` は push されるのかと思ってたらそうでもなかった。
