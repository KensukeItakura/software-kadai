# AIアシスタント付き学生生活統合管理ツール

このアプリケーションは、時間割や課題管理といった基本的な機能に加え、Google Gemini API を活用した多様なAIアシスタント機能を統合した、学生生活を強力にサポートするためのWebツールです。

## 紹介動画

[![アプリ紹介動画](https://img.youtube.com/vi/YOUR_YOUTUBE_VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=YOUR_YOUTUBE_VIDEO_ID)
*(↑ `YOUR_YOUTUBE_VIDEO_ID` の部分を、あなたのYouTube動画のIDに置き換えてください)*

## 主な機能

- **時間割管理**: ドラッグ＆ドロップで直感的に操作できる時間割機能
- **課題・ToDoリスト**: 課題や個人的なタスクを一元管理
- **AIタスク提案**: 現在の状況を分析し、次に取り組むべきタスクを提案
- **AI文章要約**: 長い文章やレポートを瞬時に要約
- **AIレポート構成案**: テーマとキーワードからレポートの骨子を自動生成
- **AI用語解説**: 分からない単語を家庭教師のように詳しく解説

## セットアップ手順

このアプリケーションは、フロントエンド（ブラウザで動作）とバックエンド（Google Colabで動作）で構成されています。

### 1. 必要なもの

- **Google Gemini APIキー**: [Google AI Studio](https://aistudio.google.com/app/apikey) から無料で取得できます。
- **ngrok 認証トークン**: [ngrokのダッシュボード](https://dashboard.ngrok.com/get-started/your-authtoken) から無料で取得できます。

### 2. バックエンドサーバーの起動 (Google Colab)

1.  このリポジトリにある `software_kadai.ipynb` ファイルをGoogle Colabで開きます。
2.  ファイル内の指示に従い、取得した **Google Gemini APIキー** と **ngrok 認証トークン** をコード内の指定された場所に入力します。
3.  Colabのセルを上から順番に実行し、サーバーを起動します。
4.  出力に表示される `https://xxxxxxxx.ngrok-free.app` のような公開URLをコピーします。このURLはサーバーを起動するたびに変わります。

### 3. フロントエンドの起動

1.  このリポジトリにある `index.html` ファイルをテキストエディタで開きます。
2.  `<script>` タグ内にある `YOUR_NGROK_URL_HERE` という部分を見つけます。
    ```javascript
    const YOUR_NGROK_URL_HERE = "https://xxxxxxxx.ngrok-free.app"; // ★★★ ここにあなたのngrok URLを貼り付け！ ★★★
    ```
3.  `"https://xxxxxxxx.ngrok-free.app"` の部分を、ステップ2-4でコピーした **あなた自身のURL** に書き換えて保存します。
4.  `index.html` ファイルをWebブラウザで開きます。

これで、全ての機能が利用可能になります。