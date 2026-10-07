---
name: pdf-mcp
description: Use when the user asks about reading, searching, extracting text/tables/charts from PDF files, or when PDF content needs to be processed. Use when the user mentions PDF-related tasks. This skill documents that @jztan/pdf-mcp is already configured as an MCP server in opencode.
---

# PDF MCP

`@jztan/pdf-mcp` が opencode の MCP 設定に追加済みです。

## 概要

PDFファイルの読み取り・検索・抽出ができるMCPサーバー。
npxで動作し、ログインやAPIキーは不要。

## 有効なツール

| ツール | 説明 |
|-------|------|
| `pdf_info` | PDFのメタデータ・ページ数・目次を取得 |
| `pdf_search` | 全文検索＆意味検索（キーワードや質問で検索） |
| `pdf_read_pages` | 指定ページのテキスト・画像・表を取得（OCR対応） |
| `pdf_read_all` | PDF全体を読む（小さいファイル向け） |
| `pdf_render_pages` | ページを画像(PNG)として出力 |
| `pdf_extract_chart` | グラフの(x, y)データを抽出 |
| `pdf_corpus_overview` | フォルダ内の全PDFを一覧 |
| `pdf_corpus_search` | フォルダ内の全PDFを横断検索 |

## 特徴

- 日本語対応（縦書きも可）
- OCR対応（スキャンPDFもテキスト化）
- テーブル抽出
- 画像抽出
- ハイブリッド検索（キーワード + セマンティック）
- ログイン不要・APIキー不要・無料

## 設定

opencode.json での設定済み:

```json
"pdf": {
  "type": "local",
  "command": ["npx", "-y", "@jztan/pdf-mcp"],
  "enabled": true
}
```
