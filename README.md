# C言語 講義の参考資料

C言語講義の参考資料を集めた静的サイトです。GitHub Pages でそのまま公開できます。

## 構成

```
index.html        資料の一覧(materials.json を読み込んで表示・検索)
materials.json    資料の一覧データ
m/<slug>.html     各資料(1資料1ファイル)
.nojekyll         Jekyll 処理を無効にする空ファイル
LICENSE           サンプルコードのライセンス(MIT)
```

## 公開手順

1. GitHub で新しいリポジトリ(例: `c-lecture`)を **Public** で作成する
2. このフォルダの中身をすべてリポジトリ直下にアップロードする(`index.html` が直下に来るようにする)
3. Settings → Pages → Build and deployment で、Source を **Deploy from a branch**、Branch を `main` / `(root)` にして Save
4. 数分後に `https://<ユーザー名>.github.io/c-lecture/` で公開される

## 資料の追加

1. `m/` に新しい資料の HTML を置く(例: `m/arrays.html`)
2. `materials.json` に次の形式で1件追加する

```json
{ "slug": "arrays", "title": "配列入門", "tag": "配列", "date": "2026-10-21", "summary": "一次元配列と添字、範囲外アクセスの注意点。" }
```

3. コミットして push する。一覧には日付の新しい順に表示される

## ローカルで確認する

`index.html` は `materials.json` を `fetch` で読み込むため、ファイルを直接開くと一覧が表示されません。

```
python3 -m http.server 8000
```

を実行して http://localhost:8000/ を開いてください。

## ライセンス

- 資料の文章・図: CC BY 4.0
- サンプルコード: MIT License(`LICENSE` を参照)
