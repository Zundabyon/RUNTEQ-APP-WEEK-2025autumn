# Git学習メモ
## 今までやってきたことここにまとめますか

* ちなみにメモはマークダウン方式使えるからめっちゃ便利です
tyantyanko

GitHubでリモートリポジトリの登録をしました
GitHub側のURLをこっちに貼り付けて連携させました。


## Railsの基本規則
①CoC Convention Over Configuration 
これに従ってやっていってください
* データベースのテーブル名はモデル名の複数形にすること
（モデル名　Fish ならテーブル名は fishes）
/fishesというURLは魚の一覧を表す
魚のID:1を表すURLは /fishes/1である

こういった規約に従うことで
* 多くの設定ファイルを書く必要がない
* 共通ルールがあることで他のエンジニアとの意思疎通がとりやすくなる

②DRY Don't Repeat Yourself
同じことを繰り返さない
見やすくなるし
メンテナンス性が高まります

③Rest Representational State Transfer
全てのリソースに一意となる識別子（URI）がある
URIを通してリソースを操作する手段を提供する
という考え方を基盤としているよ

例えば　/fishes/01 がURIが指す内容を「リソース」と呼び
魚の一覧を取得する処理は　/fishes/01へHTTPのGETメソッドでアクセスして取得します。

魚の一覧を取得する処理は　/fishes/01へHTTPのGETメソッドでアクセスして取得します。