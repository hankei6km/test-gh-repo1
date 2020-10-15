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

## gh pr

`$ gh pr create` すると幾つかの質問に回答後、ローカルで開いているブランチで作成される。

コメントは `$ gh pr review --commwent -b 'コメント'` で作成するようだが、
コメントを参照する方法は(`$ gh pr view` で参照できない?)


`$ gh pr merge -m` で(デフォルトだと)ローカルとgithub 上のブランチは削除される(`origia/????` のブランチは削除されない).

```console
$ gh pr merge -m
✔ Merged pull request #1 (Note gh repo create)
✔ Deleted branch topic/note-repo-create and switched to branch master

$ git fetch origin --prune
From github.com:hankei6km/test-gh-repo1
 - [deleted]         (none)     -> origin/topic/note-repo-create
```

このブランチはコンフリクトする状態で `$ gh pr create` してみた。
ウェブ上では以下のように表示されているが `gh` からはどう確認する?

> This branch has conflicts that must be resolved
