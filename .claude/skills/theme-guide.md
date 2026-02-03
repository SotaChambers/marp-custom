---
description: KGモーターズ Marpテーマの使い方ガイド。スライドクラス、コンポーネント、カラートークンの説明と使用例を提供する。
---

# KGモーターズ テーマガイド

このスキルはtheme/theme.cssの使い方を説明します。

## スライドクラス

### title（カバースライド）
左右分割レイアウト。左に会社名・日付、右にカスタム画像。

```markdown
---
marp: true
theme: theme
class: title
size: 16:9
footer: "(C) KG motors INC. All Rights Reserved."
---

# プレゼンタイトル

会社名

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
デフォルト。class指定なし、または空で使用。

```markdown
---
<!-- class: -->

# スライドタイトル

本文
```

## カラートークン

| トークン | 値 | 用途 |
|---------|-----|------|
| `--kg-yellow` | #f5c518 | ブランドカラー、アクセント |
| `--kg-black` | #1a1a1a | メインテキスト |
| `--kg-charcoal` | #3d3d3d | サブテキスト、ヘッダー背景 |
| `--kg-body-text` | #4a4a4a | 本文テキスト |
| `--kg-gray-100` | #f5f5f5 | 背景（薄いグレー） |
| `--kg-gray-200` | #e0e0e0 | ボーダー |

## コンポーネント

### コールアウト（kg-callout）
注釈やポイントを強調。

```html
<div class="kg-callout">
<strong>ポイント：</strong> 重要な説明文
</div>

<div class="kg-callout warning">
<strong>注意：</strong> 警告文
</div>
```

### 2カラムレイアウト（kg-two-col）
左右に分割して表示。

```html
<div class="kg-two-col">
<div class="col">

### 左カラム
- 項目1
- 項目2

</div>
<div class="col">

### 右カラム
- 項目A
- 項目B

</div>
</div>
```

### テーブル（kg-table）
スタイル付きテーブル。

```html
<table class="kg-table">
<thead>
<tr><th>項目</th><th>値</th></tr>
</thead>
<tbody>
<tr><td>データ1</td><td>100</td></tr>
<tr><td>データ2</td><td>200</td></tr>
</tbody>
</table>
```

### バッジ（kg-badge）
ラベルやタグ表示。

```html
<span class="kg-badge">新機能</span>
<span class="kg-badge dark">重要</span>
```

### 区切り線（kg-divider）
セクション間の区切り。

```html
<hr class="kg-divider">
```

### スペック表示（kg-spec）
ラベルと値のペア表示。

```html
<div class="kg-spec">
<span class="kg-spec-label">乗車定員</span>
<span class="kg-spec-value">1名</span>
</div>
```

### 情報パネル（kg-info-panel）
番号付きラベルと箇条書き。

```html
<div class="kg-info-panel">
  <div class="kg-info-panel-label">1. 開発内容</div>
  <div class="kg-info-panel-content">
    <ul>
      <li>項目1</li>
      <li>項目2</li>
    </ul>
  </div>
</div>
```

### カード（kg-card）
ヘッダー付きカード。

```html
<div class="kg-card">
  <div class="kg-card-header">
    カードタイトル
  </div>
  <div class="kg-card-body">
    <strong>見出し</strong>
    <ul>
      <li>項目1</li>
      <li>項目2</li>
    </ul>
  </div>
</div>
```

## 指示

ユーザーがスライド作成で困っている場合：
1. 適切なスライドクラス（title/top/main）を提案
2. 情報の種類に合ったコンポーネントを推奨
3. 具体的なHTML/マークダウンのコード例を提供
