# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

Marpを使用したプレゼンテーション作成プロジェクト。KGモーターズ社向けのカスタムテーマを含む。

## スラッシュコマンド

### Commands
- `/generate-slide` - スライド生成（title/top/mainテンプレート）
- `/export_pdf <file.md>` - PDFにエクスポート
- `/test_slide <file.md>` - スライドの品質チェック

### Skills
- `/theme-guide` - テーマ・コンポーネントの使い方ガイド
- `/design-review` - スライドデザインのレビュー・改善提案
- `/convert-to-marp` - テキスト資料をMarpスライドに変換

## プレビュー

VS Code + Marp拡張機能を使用。マークダウンファイルを開いてプレビューパネルを表示。

## テーマシステム（theme/theme.css）

単一CSSファイルでスライドの種類をclass切り替えで実装:
- **main**（デフォルト）: class指定なし - 通常のコンテンツスライド
- **title**: `<!-- class: title -->` - 左右分割のカバースライド
- **top**: `<!-- class: top -->` - 黄色背景のセクション区切り

詳細は `/theme-guide` を参照。

## ディレクトリ構成
- `theme/` - Marpカスタムテーマ
- `imgs/` - スライドで使用する画像
- `input/` - 入力ファイル用
- `output/` - エクスポートされたファイル用
