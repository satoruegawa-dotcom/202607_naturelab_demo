# NatureLab Creative DEMO

ネイチャーラボ向け広告クリエイティブ分析・バナー生成DEMOです。静的HTML構成のため、ビルド処理なしでVercelへ公開できます。

## GitHubへ登録

この `vercel-deploy` フォルダの中身をリポジトリのルートとして登録してください。

```bash
git init
git add .
git commit -m "Add NatureLab creative demo"
git branch -M main
git remote add origin <GitHubリポジトリURL>
git push -u origin main
```

## Vercelへ公開

1. Vercelで `Add New > Project` を選択
2. 上記GitHubリポジトリをImport
3. Framework Presetは `Other`
4. Root Directoryはリポジトリ直下なら `./`
5. Build CommandとOutput Directoryは未指定
6. `Deploy` を実行

## 画面構成

- `index.html`：iframeルーター・エントリーポイント
- `admin.html`：クリエイティブ管理画面
- `detail.html`：主採用クリエイティブ詳細
- `detail2.html`：探索クリエイティブ詳細
- `generate.html`：新規生成画面
- `public/assets/creative/`：使用中のバナー画像6枚

## 注意

- Tailwind CSS、DECAロゴ、アバターは外部CDNから読み込みます。公開環境ではインターネット接続が必要です。
- `vercel.json`で検索エンジンのインデックスを抑止しています。機密情報を保護する認証機能ではありません。
- URLを限定共有したい場合は、Vercel側のDeployment Protectionを設定してください。