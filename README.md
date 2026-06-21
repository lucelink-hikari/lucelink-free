# lucelink-free

LuceLink Free（ルーチェリンク フリー）は、iPhone / Android 向けの AI チャットアプリです。

OpenRouter 経由で GPT / Claude / Gemini / Grok などの AI モデルと会話できます。自分だけの AI パートナーや作業環境を、スマホで手軽に育てられます。

## 特徴

- **スマホ特化** — iPhone Safari / Android Chrome で動く PWA アプリ
- **プリセット** — AI ごとにシステムプロンプト・メモリ・知識ファイルを設定できる
- **バックアップ** — 会話履歴や設定を ZIP で書き出し・復元
- **プライバシー** — 会話はすべて端末のブラウザ内に保存。開発者がデータを見ることはありません

## 詳しい説明

- [LuceLink Free の機能説明](https://note.com/magic_stork7986/n/n68fe47ad1c20)
- [セットアップ手順](https://note.com/magic_stork7986/n/nf9e19ddc48ba)
- [質問・不具合報告はこちら](https://note.com/qa/magic_stork7986)

## 必要なもの

- iPhone または Android スマートフォン
- [OpenRouter](https://openrouter.ai/) のアカウントと API キー
- [Cloudflare](https://dash.cloudflare.com/) のアカウント
- OpenRouter で利用するクレジット（残高）

## セットアップの流れ

1. OpenRouter で API キーを作成する
2. 配布 ZIP 内の Worker コードをコピーする
3. Cloudflare で Worker を新規作成し、コードを貼り付けてデプロイする
4. Worker の Settings → Variables and Secrets に `OPENROUTER_API_KEY` を Secret として登録する
5. Worker URL の末尾に `/api/healthz` を付けて開き、正常応答を確認する
6. LuceLink Free の公開 URL を開き、設定画面で Worker URL を入力して接続確認する
7. ホーム画面に追加して PWA として使う

詳しい手順は、配布 ZIP 内の README・セットアップガイド、および note の解説記事に記載しています。

## 注意事項

- API 利用料金・通信費は、利用者ご自身の負担です
- 会話履歴や設定はブラウザ内に保存されます。ブラウザデータの削除や端末変更でデータが失われる可能性があります。**こまめなバックアップをお願いします**
- データが消えた場合、開発者は責任を負いかねます
- AI の回答は正確とは限りません。医療・法律・金融など重要な判断には専門家の確認を行ってください
- 個人情報や機密情報など、外部へ送信したくない内容は入力しないでください

## 対応環境

- **iPhone** — Safari / PWA で動作確認しています
- **Android** — 端末やブラウザにより、ホーム画面への追加やファイル保存の挙動が異なる場合があります

## LuceLink Plus（有料版）

Free 版の機能に加え、より長く AI パートナーと暮らしていくための機能を備えた有料版があります。

- OpenAI / Anthropic / Google / xAI の各社公式 API に対応
- 全テーマ（15種類）
- 画像送信（対応モデルのみ）
- お気に入り（会話の吹き出しを星で登録）
- ChatGPT / Claude 公式エクスポートの Import

Plus 版は note にて販売しています。
**購入前に、必ず Free 版で導入と動作確認を済ませてください。**

## ライセンス

個人利用のみ許可しています。再配布・転売・二次配布は禁止です。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

## フィードバック

使ってみた感想、不具合報告、質問は質問箱からお寄せください。  
個別の導入代行や環境設定のサポートには対応できない場合があります。

© そらとひかり
