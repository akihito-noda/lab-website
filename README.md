# Lab Website Template for GitHub Pages

GitHub Pages + Jekyll 用の研究室Webサイトひな形です。

## 使い方

1. GitHubで新しいリポジトリを作成します。
2. このフォルダの中身をリポジトリにアップロードします。
3. GitHubの `Settings > Pages` で公開元を設定します。
   - Branch: `main`
   - Folder: `/ (root)`
4. 数分後にGitHub PagesのURLで公開されます。

## 主な編集箇所

- `_config.yml`: サイト名、説明、URL設定
- `_data/members.yml`: メンバー一覧
- `_data/publications.yml`: 業績一覧
- `_data/news.yml`: ニュース一覧
- `research.md`: 研究テーマ
- `for-students.md`: 配属希望者向け説明
- `access.md`: アクセス・連絡先

## ローカル確認

Rubyが利用できる環境では、以下でローカル確認できます。

```bash
bundle install
bundle exec jekyll serve
```

ブラウザで `http://localhost:4000` を開きます。
