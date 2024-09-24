# MISTEMS is Misskey Fork System

ほしい機能詰め込みMisskey

## 変更点

このPRをだいたいぜんぶ入れる
https://github.com/mistems/mistems/pulls

- 投稿フォーム
  - チャンネルピッカー　追加
  - 宛先チャンネル表示　追加
  - CWと本文の入れ替えボタン　追加
- チャンネル一覧
  - だいたいぜんぶみるタブ　追加（もっと→チャンネル）

- チャンネル周り全般
  - 既存の投稿ボタンと通常公開範囲の投稿ボタンを両方置く

- ショートカットキー
  - h でショートカットキーヘルプ

# 開発者向けドキュメント
## MISTEMSの作り方

### システムブランチ

- mistems-admin  - misskey/develop となんとなく一致させる
- mistems-main  - 後述の方法で misskey/develop 最新に機能ブランチを取り込んだブランチ デプロイするときはこれを使う コミットログはあまり当てにならない
- mistems-readme - READMEが置いてあるだけで何も無い

### ブランチの取り込み方
PRのと見込みはGitHub上ではなくローカルで行う
```
git merge --squash 任意ブランチ
git commit -a -m "メッセージ"
```

### squash マージ同士の共存（コンフリクトの解除）
コンフリクトした場合、適宜解決する
が、毎回コンフリクト解除するのはやってられないので、 git rerere に乗っかる

【Git】同じコンフリクト解消を繰り返している人に教えたい「git rerere」 #初心者 - Qiita https://qiita.com/_ken_/items/64856e91e062b325590f

### 機能ブランチを最新に追従させる方法
git mergeではなくgit rebaseを使わなかればならない
（squashでのコンフリクト解決が困難になるはず）




