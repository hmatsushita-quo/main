機密コードの分離の実装案

[git-submodule](https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%81%95%E3%81%BE%E3%81%96%E3%81%BE%E3%81%AA%E3%83%84%E3%83%BC%E3%83%AB-%E3%82%B5%E3%83%96%E3%83%A2%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB)


やること
- quo-infinity-secretに機密性が高いと判断された処理を実装（元々の内容を追加）
- 上記のテストコードを追加
- 上記リポジトリの参照及び書き込み権限をqubeチームに限定してもらう
- qube-managerにてgit-submoduleとして上記のリポジトリへの参照を追加
- ビルドスクリプトの過程で以下の内容を追加
- sub-moduleの内容を最新化するためのコマンド
```yml
git submodule update --init --recursive
```

[参考](https://qiita.com/ma2saka/items/4bd00ef6f8c240847807#git-submodule-update---init----recursive-%E3%81%A7%E5%86%8D%E5%B8%B0%E7%9A%84%E3%81%AB%E6%9B%B4%E6%96%B0%E3%81%99%E3%82%8B)