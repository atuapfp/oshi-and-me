# 推しとわたし診断

推し活テーマの診断風ホラー（ヤンデレ）ゲーム。静的サイト（HTML/CSS/JSのみ・ビルド不要）。

## 公開手順（GitHub Pages）
1. GitHubで新しいリポジトリを作成（無料プランはPublic必須）。例: `oshi-and-me`
2. 公開URLを決める: `https://<GitHub ID>.github.io/<リポジトリ名>/`（末尾の `/` 必須）
3. **全ファイル内の `https://atuapfp.github.io/oshi-and-me/` を、上のURLに置換**する（`index.html` と `result/*/index.html`）
   - Mac/Linux: `grep -rl https://atuapfp.github.io/oshi-and-me/ . | xargs sed -i 's|https://atuapfp.github.io/oshi-and-me/|https://ID.github.io/REPO/|g'`
   - 置換前は共有文にURL行が出ず、OGPも無効になります
4. リポジトリ直下に全ファイルを置いて push
5. Settings → Pages → Source: `Deploy from a branch` / `main` / `/ (root)` を保存
6. 数分後に公開URLを開いて動作確認。X（Twitter）の Card Validator 等でOGPを確認

## 構成
- `index.html` 本体
- `result/<type>/index.html` 結果タイプ別ページ（SNSカード用。人が開くと本体へ移動）
- `ogp/*.png` OGP画像 (1200×630)
- `.nojekyll` Jekyll処理を無効化

## 補足
- 回答・行動データはすべて端末内のみ（localStorage `oshi-to-watashi-v1`）。外部送信なし。
- 複製対策をしたい場合は、READMEにLICENSE（例: All rights reserved）や「無断転載禁止」を明記すると抑止になります。
- 診断はフィクションの娯楽です。医学的診断ではありません。
