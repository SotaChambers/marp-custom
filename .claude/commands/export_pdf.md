# PDF出力

マークダウンファイルをPDFにエクスポートします。

## コマンド

```bash
npx @marp-team/marp-cli $ARGUMENTS --theme theme/theme.css --allow-local-files -o output/$(basename "$ARGUMENTS" .md).pdf
```

## 引数

- `$ARGUMENTS`: 対象のマークダウンファイル（例: sample.md）

## 実行例

```bash
# sample.mdをPDFにエクスポート
npx @marp-team/marp-cli sample.md --theme theme/theme.css --allow-local-files -o output/sample.pdf
```

## 指示

1. 引数が指定されていない場合、カレントディレクトリの.mdファイルを一覧表示して選択させる
2. エクスポート実行前にファイルの存在を確認
3. 出力先は `output/` ディレクトリ
4. エクスポート完了後、出力ファイルのパスを表示
