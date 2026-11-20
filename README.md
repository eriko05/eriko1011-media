# お客さま専用 動画ライブラリ（長田絵里子）

お客さまにURLを送って、好きな時間に見てもらうための動画ページです。

## ファイル構成
- index.html … 動画ライブラリのページ（CSSとJavaScriptも中に入っています）
- images/profile.jpg … サムネイルに入れているプロフィールのイラスト
- vercel.json … Vercel の設定（アドレスの最後に `/` を付ける、検索エンジンに載せない）

## 公開
- Vercel で公開しています。`main` ブランチに変更が入ると自動で更新されます。
- 検索結果に出ないよう、ページの `<meta name="robots">` と `vercel.json` の `X-Robots-Tag` で指定しています。
  URLを知っている人は誰でも見られるので、URLはお客さまにだけ送ってください。

## 動画の追加・変更
`index.html` の中ほどにある `const ITEMS = [` のリストに、1本ずつ追加します（上にあるものほど新しい扱い）。
- `url`：YouTube のURL（「限定公開」にする）、Googleドライブの共有URL など
- `title`・`category`・`desc`：タイトル、カテゴリ、説明文
- `kicker`・`catch`：サムネイルの左上の札と大きい文字（`**ここ**` が強調、`\n` が改行）
- `featured:true` を付けた動画が、トップの大きい枠に出ます
