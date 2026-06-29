# 介護AI Assistant

介護士がAIと会話するだけで、通常記録・事故報告書を作成できるWebアプリ。

- **API不要** — Ver1はルールベースで動作（OpenAI/Claude API差し替え可能な設計）
- **iPad Safari 最適化** — タッチ操作・セーフエリア・キーボード音声入力対応
- **単一HTMLファイル** — サーバー不要、ブラウザで開くだけ

## デモ

👉 **https://〈kyon41chi10-wq〉.github.io/care-ai-assistant/**

## 使い方

1. 利用者を選択
2. 入力種別（通常記録AI / 事故報告書AI）を選択
3. 「会話をはじめる」をタップ
4. AIと会話 → 記録が自動生成 → 各項目をコピー

## 機能

| 機能 | 説明 |
|------|------|
| 通常記録AI | 日々の様子をCAREKARTEへ貼り付ける記録を生成 |
| 事故報告書AI | 転倒・転落・誤嚥等の事故報告書（4カード）を生成 |
| クイック選択肢 | 「外傷なし」「看護師」等の定型回答をワンタップで送信 |
| 取得済み情報バー | AIが把握した情報をリアルタイム表示 |
| 編集・再生成・コピー | 生成文はその場で修正・別表現へ切替・個別コピー可能 |

## ローカルで開く

```bash
git clone https://github.com/〈ユーザー名〉/care-ai-assistant.git
open care-ai-assistant/index.html   # macOS
# または index.html をブラウザにドラッグ&ドロップ
```

## 将来のAPI接続

`app.js` 内の1行を差し替えるだけで接続できます。

```js
// 現在（Ver1 / ルールベース）
ai: new MockAIService(),

// OpenAI GPT-4o に切り替える場合
ai: new OpenAIService("sk-..."),
```

`OpenAIService` のひな形は `index.html` 内コメントに記載済みです。

## ライセンス

MIT
