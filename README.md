# ふじわら内装 — Webサイト

広島県福山市の内装工事専門店「ふじわら内装」の公式Webサイト。  
GitHub Pages で無料公開。

## ファイル構成

```
naiso-fujiwara/
├── index.html   ← メインページ（すべてここに入っている）
└── README.md    ← この説明書
```

## GitHub Pages で公開する手順

### 1. GitHubにリポジトリを作成

1. https://github.com を開いてログイン
2. 右上「+」→「New repository」
3. Repository name: `naiso-fujiwara`（または好きな名前）
4. Public を選択
5. 「Create repository」をクリック

### 2. このフォルダをGitHubにアップロード

ターミナル（コマンドプロンプト）で以下を実行：

```bash
cd C:\Users\minor\naiso-fujiwara
git init
git add .
git commit -m "内装業HP 初回公開"
git branch -M main
git remote add origin https://github.com/【あなたのGitHubユーザー名】/naiso-fujiwara.git
git push -u origin main
```

### 3. GitHub Pages を有効にする

1. GitHubのリポジトリページを開く
2. 「Settings」タブをクリック
3. 左メニュー「Pages」をクリック
4. Source: 「Deploy from a branch」を選択
5. Branch: `main` / `/ (root)` を選択
6. 「Save」をクリック

数分後、以下のURLでサイトが公開されます：  
`https://【GitHubユーザー名】.github.io/naiso-fujiwara/`

## 内容の変更方法

`index.html` を直接編集してください。

### 必ず変更が必要な箇所

| 場所 | 変更内容 |
|------|---------|
| `090-XXXX-XXXX` | 実際の電話番号に変更（4か所） |
| 施工写真のプレースホルダー | 実際の写真に差し替え |
| `20年以上` | 実際の経験年数に変更 |
| 福山市・尾道市・笠岡市 | 実際の対応エリアに変更 |
| フォームのaction属性 | Formspree等のURLを設定（後述） |

### お問い合わせフォームの送信先を設定する（無料）

1. https://formspree.io でアカウント作成
2. 「New Form」でフォームを作成
3. 表示されたエンドポイントURL（例: `https://formspree.io/f/xxxxxxxx`）をコピー
4. `index.html` の `<form action="#">` を `<form action="https://formspree.io/f/xxxxxxxx">` に変更
5. `method="POST"` のままでOK

## CODEXへの指示例

Claude Code（CODEX）に追加・変更を依頼する場合：

- 「施工実績セクションをindex.htmlに追加して。ビフォーアフター写真2枚を並べるレイアウトで」
- 「電話番号を090-1234-5678に変更して」
- 「対応エリアに三原市を追加して」
- 「色を緑系に変えて」
