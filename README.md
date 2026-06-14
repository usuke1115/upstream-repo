- `upstream-repo` リポジトリは本家のリポジトリ
- `fork-repo` は fork して `upstream-repo` の変更を取り込みたい側のリポジトリ

`upstream-repo` 側ではいつも通りの操作をすればいいので、問題なし。

# `fork-repo` で `upstream-repo` の変更を取り込む手順
```
$ git remote -v

$ git remote rename origin upstream

$ git fetch upstream

$ git merge upstream/main

$ git remote rename origin upstream

$ git remote add origin <fork-repoのURL>
```

`git remote rename origin upstream`は `origin` を `upstream` に変えるコマンドである。

