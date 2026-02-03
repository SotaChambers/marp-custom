# KGモーターズ Marpスライドテンプレート

Marpを使用したプレゼンテーション作成テンプレート。KGモーターズのブランドカラーとデザインガイドラインに沿ったカスタムテーマを含みます。

## セットアップ

### 必要なもの
- [VS Code](https://code.visualstudio.com/)
- [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) 拡張機能

### インストール
1. VS Codeで本リポジトリを開く
2. Marp拡張機能をインストール
3. `.vscode/settings.json` でカスタムテーマが自動的に読み込まれる

## 使い方

### プレビュー
マークダウンファイルを開き、右上のプレビューアイコンをクリック。

### エクスポート
```bash
# PDFにエクスポート
npx @marp-team/marp-cli sample.md --theme theme/theme.css -o output/sample.pdf

# HTMLにエクスポート
npx @marp-team/marp-cli sample.md --theme theme/theme.css -o output/sample.html

# PPTXにエクスポート
npx @marp-team/marp-cli sample.md --theme theme/theme.css -o output/sample.pptx
```

## スライドクラス

### title（カバースライド）
左右分割レイアウト。プレゼンの表紙に使用。

```markdown
---
marp: true
theme: theme
class: title
size: 16:9
footer: "(C) KG motors INC. All Rights Reserved."
---

# プレゼンタイトル

KGモーターズ株式会社

YYYY/MM/DD

![ロゴ](./imgs/KG_LOGO_SMALL.png)
![カスタム](./imgs/mibot.png)
```

### top（セクション区切り）
黄色背景。セクションの区切りに使用。

```markdown
---
<!-- class: top -->

# 01 | セクション名
```

### main（通常コンテンツ）
デフォルト。class指定なしで使用。

```markdown
---
<!-- class: -->

# スライドタイトル

本文テキスト
```

## コンポーネント

### コールアウト
```html
<div class="kg-callout">
<strong>ポイント：</strong> 重要な説明文
</div>

<div class="kg-callout warning">
<strong>注意：</strong> 警告文
</div>
```

### 2カラムレイアウト
```html
<div class="kg-two-col">
<div class="col">

### 左カラム
- 項目1

</div>
<div class="col">

### 右カラム
- 項目A

</div>
</div>
```

### その他のコンポーネント
- `kg-table` - スタイル付きテーブル
- `kg-spec` - スペック表示（ラベル+値）
- `kg-info-panel` - 番号付きラベル+箇条書き
- `kg-card` - ヘッダー付きカード
- `kg-badge` / `kg-badge dark` - バッジ
- `kg-divider` - 区切り線

詳細は `theme/theme.css` を参照。

## ディレクトリ構成

```
.
├── theme/          # Marpカスタムテーマ
│   └── theme.css
├── imgs/           # スライドで使用する画像
├── input/          # 入力ファイル用
├── output/         # エクスポートされたファイル用
├── sample.md       # サンプルスライド
└── .vscode/        # VS Code設定
```

## カラーパレット

| カラー | コード | 用途 |
|--------|--------|------|
| KG Yellow | `#f5c518` | ブランドカラー、アクセント |
| KG Black | `#1a1a1a` | メインテキスト |
| KG Charcoal | `#3d3d3d` | サブテキスト、ヘッダー背景 |
