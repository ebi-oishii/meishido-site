# meishido-site

「名刺道」の GitHub Pages 公開サイトです。national-team-site と同じ Jekyll パターン。

## 公開 URL（GitHub Pages 有効化後）

| ページ | URL |
| --- | --- |
| トップ | `https://ebi-oishii.github.io/meishido-site/` |
| サポート | `https://ebi-oishii.github.io/meishido-site/support/` |
| プライバシー | `https://ebi-oishii.github.io/meishido-site/privacy/` |
| 利用規約 | `https://ebi-oishii.github.io/meishido-site/terms/` |
| 特商法 | `https://ebi-oishii.github.io/meishido-site/commerce/` |
| 免責事項 | `https://ebi-oishii.github.io/meishido-site/disclaimer/` |

App Store Connect / Google Play Console にはこれらの URL を登録します。

## GitHub リポジトリ作成 → Pages 有効化手順

1. **GitHub でリポジトリ作成**
   - リポジトリ名: `meishido-site`
   - 公開範囲: **Public**（GitHub Pages は Free プランでは Public のみ）
   - README/`.gitignore`/LICENSE は追加しない（後で push するので）

2. **ローカルからリポジトリを push**
   ```bash
   cd /Users/taiichi/workspace/meishido-site
   git init
   git add .
   git commit -m "初期公開: プライバシー・利用規約・特商法・免責・サポート"
   git branch -M main
   git remote add origin git@github.com:ebi-oishii/meishido-site.git
   git push -u origin main
   ```

3. **GitHub Pages 有効化**
   - GitHub の該当リポジトリ → **Settings** → **Pages**
   - **Build and deployment** → **Source** を `Deploy from a branch`
   - **Branch** を `main` / `/ (root)` に設定して **Save**
   - 数分待つ → 上記 URL で公開確認

4. **AdMob 側の設定**（該当する場合）
   - AdMob 管理画面で本アプリを登録し、**app-ads.txt の検証** を実行
   - `app-ads.txt` はデベロッパー Web サイトのルートに置く必要あり
   - プロジェクトサイト URL (`https://ebi-oishii.github.io/meishido-site/app-ads.txt`) はサブパスなので、AdMob は通常「デベロッパーサイト」= `ebi-oishii.github.io/app-ads.txt` を参照する点に注意
   - ebi-oishii.github.io のルートに app-ads.txt を配置するのが確実（既に national-team-site 側で対応済みかも）

## app-ads.txt

同一パブリッシャーの複数アプリを扱う場合、内容は同じ。

```
google.com, pub-9837264864279123, DIRECT, f08c47fec0942fa0
```

## サポート窓口

- `ebi.apps.support@gmail.com`

## メンテナンス

- 情報が変更されたら該当 `.md` の **最終更新日** と本文を更新して push
- 大きな変更（利用者への影響がある場合）は「制定日」も更新
