# YYRP情報局 サイト一式

## ファイル構成
```
(リポジトリのルート)
├── index.html      ← HOME（検索ページ）
├── craft.html       ← クラフト早見表
├── freeca.html       ← フリーカ強盗ページ
├── bobcat.html       ← ボブキャットページ
└── vehicles/         ← 車両リスト（yyrp-vehicle-list の中身をここに入れる）
    ├── index.html
    ├── vehicles.json
    ├── favicon.svg
    ├── logo.png
    └── .nojekyll
```

## 手順（既存の yyrp-vehicle-list リポジトリに統合する場合）

1. 既存リポジトリ（auto3333333333/yyrp-vehicle-list）の中身を、新しく作る `vehicles/` フォルダに移動する
   - `index.html`, `vehicles.json`, `favicon.svg`, `logo.png`, `.nojekyll` を `vehicles/` フォルダへ
   - `CNAME` はリポジトリのルートに残す（ドメイン設定はそのまま使えます）
2. このzipに入っている `index.html`, `craft.html`, `freeca.html`, `bobcat.html` をリポジトリのルートに置く
3. コミットしてpush（またはGitHubのWeb UIで「Add file」→「Upload files」からドラッグ＆ドロップ）
4. GitHub Pages の設定でルートディレクトリが公開対象になっていればOK
5. 反映後、`https://yyvl.auto3develop.tech/` がHOMEページに、`https://yyvl.auto3develop.tech/vehicles/` が車両リストになります

## 新しく別リポジトリを作る場合

同じファイル構成のまま新規リポジトリを作り、GitHub Pagesを有効化するだけでOKです。

## 今後ページを追加するとき

`freeca.html` や `bobcat.html` と同じ構造でファイルを増やし、`index.html` 内の該当カードの
`href="準備中"` の部分を作成したファイル名（例: `combini.html`）に書き換えれば導線がつながります。
