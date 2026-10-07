# Nanbeige llama-server 操作手順

## 使う前に

```bash
cd /Users/fur-dev/.config/opencode/local-llm
```

## 操作一覧

| やりたいこと | コマンド |
|---|---|
| サーバー起動 | `make -f Makefile.nanbeige on` |
| サーバー停止 | `make -f Makefile.nanbeige off` |
| 状態確認 | `make -f Makefile.nanbeige status` |
| 再起動 | `make -f Makefile.nanbeige restart` |
| ログを見る | `make -f Makefile.nanbeige logs` |
| ログ削除 | `make -f Makefile.nanbeige clean` |

## ショートカット版（スクリプト）

```bash
./nanbeige on
./nanbeige off
./nanbeige status
./nanbeige restart
./nanbeige logs
```

## 備考

- サーバーは port 6060 で起動します
- コンテキストサイズ: 65536 tokens
- モデル: Nanbeige4.2-3B Q4_K_M (2.4GB)
- 自動起動設定: launchd（ログイン時に自動起動）
