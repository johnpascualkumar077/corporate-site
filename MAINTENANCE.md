# サイト運用・更新マニュアル

このリポジトリのWebサイト（Corporate Site）を運用・更新するためのガイドです。

## 1. お知らせ (News) の更新方法
`index.html` 内の `<!-- お知らせ (News) -->` セクションを探します。
新しいお知らせを追加するには、以下の構造をコピーしてリストの先頭に追加してください：

```html
<a href="#" class="list-group-item list-group-item-action p-3">
    <div class="d-flex w-100 justify-content-between">
        <h6 class="mb-1 fw-bold text-primary">カテゴリ（例：ニュースリリース）</h6>
        <small class="text-muted">YYYY.MM.DD</small>
    </div>
    <p class="mb-1">ここに内容を記述します。</p>
</a>
```

## 2. デザインのカスタマイズ
`index.html` の `<style>` タグ内にある `:root` 変数を変更することで、サイト全体のテーマカラーを一括で変更できます。

- `--primary-color`: ナビゲーションバーや背景のメインカラー
- `--accent-color`: ボタンやリンクのアクセントカラー

## 3. GitHub Pages への反映方法
ローカルでファイルを編集した後、以下の手順で変更を反映させます：

1.  変更をステージング： `git add .`
2.  コミット： `git commit -m "更新内容のメッセージ"`
3.  プッシュ： `git push origin main`

プッシュ後、数分以内に反映されます。

## 4. ダークモードの仕組み
ユーザーがナビゲーションバーの「月/太陽」アイコンをクリックすると、`data-bs-theme="dark"` または `light` が `<body>` タグに付与されます。
スタイルは CSS 内の `[data-bs-theme="dark"] body` セクションで定義されています。
