# スライド生成

指定されたテンプレートタイプで新しいスライドを生成してください。

## テンプレートタイプ

### title（カバースライド）
```markdown
---
marp: true
theme: theme
class: title
size: 16:9
footer: "(C) KG motors INC. All Rights Reserved."
---

# タイトル

会社名

YYYY/MM/DD

![ロゴ](./imgs/KG_LOGO_SMALL.png)
![カスタム](./imgs/mibot.png)
```

### top（セクション区切り）
```markdown
---
<!-- class: top -->

# 00 | セクションタイトル
```

### main（通常コンテンツ）
```markdown
---
<!-- class: -->

# スライドタイトル

本文テキスト
```

## 指示

1. ユーザーにテンプレートタイプ（title/top/main）を確認
2. タイトルや内容をヒアリング
3. 適切なマークダウンを生成
4. 必要に応じてコンポーネント（kg-callout, kg-card等）を提案
