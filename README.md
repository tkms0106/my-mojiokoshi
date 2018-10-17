# README

Railsアプリとしては単純で

* 画像アップロードフォームを設置したページ
* 画像から読み取った文字列を表示するページ

があるだけ。

画像から文字を読み取るのはGoogle Cloud Vision APIにやってもらう。Ruby用のクライアントライブラリがあるのでGemfileに書けばよい。

```gemfile
gem 'google-cloud-vision'
```

また、GCPでプロジェクトを用意し、Cloud Vision API用のサービスアカウントを作成し、鍵をリポジトリのどこかに置いておく（.gitignoreに追加する）。ライブラリのコードを呼び出す際に鍵のパスが必要だが、このリポジトリではパスの直書きを回避するのにEncrypted Credentialsを使っている。
