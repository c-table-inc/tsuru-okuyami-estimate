# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

お悔やみ情報 CATV配信システム - 都留市役所から送信されるお悔やみ情報（PDF）を自動的にパワーポイントに変換し、CATVで放映できる形式で配信するシステム。

## アーキテクチャ

### システムフロー
```
市役所 --[PDF添付メール]--> システム --[パワポ生成]--> 市担当者 --[承認]--> CATV
```

### 技術スタック（予定）
- **バックエンド**: Laravel (PHP)
- **PDF解析**: Python (PyMuPDF / pdfplumber)
- **パワポ生成**: python-pptx
- **管理画面**: Laravel + Blade / Vue.js
- **データベース**: MySQL
- **メール受信**: AWS SES / Mailgun
- **インフラ**: AWS (EC2 or Lambda) / VPS

## ファイル構成

- `spec-okuyami-catv.md` - システム仕様書
- `proposal-okuyami-catv.html` - 提案資料（Tailwind CSS、スライド形式）
- `img/` - 画像ファイル（ロゴ、フロー図）

## 提案資料の編集

提案資料はTailwind CSSベースのHTML形式。ブラウザで開いてスライド操作可能：
- 矢印キー（←→）またはスペースでページ送り
- 右上の「印刷」ボタンでPDF出力可能
