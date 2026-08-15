# dance-assets

seevio.ai (Seedance) APIの `reference-to-video` に渡す、公開URLが必要なダンスモーション参照動画専用フォルダ。

- `dance-01-depth.mp4` — `元ダンス/img1_img2_KPOPBPM120_img1_3img_Seedance_20_Mini_82024.mp4` をDepth Anything V2で単眼深度推定した深度マップ動画(近い=明るい、遠い=暗い。色・質感情報を落とし、シルエットと動作のみを参照素材として使う意図)。

**このフォルダだけ**を独立したGitHubリポジトリとして公開する想定。`automation/`側の秘密情報(APIキー等)とは完全に分離すること。

## 公開手順(ユーザー本人が実施)

1. GitHub上でこのフォルダの内容を新規リポジトリ(public)として作成・push。
2. 生成された `https://raw.githubusercontent.com/<user>/<repo>/<branch>/dance-01-gray.mp4` のようなURLを、`automation/dance-config.json` の `videoUrls` に設定する。
