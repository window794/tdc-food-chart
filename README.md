# TDC FOOD CHART ／ 探る昼とめぐる夜

フードを、星図から探す。

トーキョー・ディスカバリー・シティ「探る昼とめぐる夜」のコラボフード（QuizKnock 考案メニュー・全40件）を検索するための非公式ツールです。

**サイト:** https://window794.github.io/tdc-food-chart/

> このコラボは既に終了しています。記録・アーカイブとしてご利用ください。

---

## 機能

- **検索** — メニュー名・店舗・エリア・考案者・コースターを横断してリアルタイムに絞り込み
- **絞り込み** — コースター種別（ボイス / 謎 / クイズ）と A・B、エリア、店舗、考案者、価格帯
- **閉店店舗の扱い** — `is_closed` に基づいて「閉店」を表示。閉店店舗を含める／含めないを切り替え可能
- **並び替え** — エリア順、価格順、メニュー名順、店舗名順、考案者順
- **詳細表示** — タイルを選ぶと店舗ページへのリンク付きの詳細を表示
- **CSV 出力** — 検索結果をダウンロード（BOM 付き UTF-8）
- **PWA** — ホーム画面に追加してアプリのように利用可能。シェルとデータをキャッシュするためオフラインでも閲覧可

## PWA としてインストールする

- **Chrome / Edge** — アドレスバー右端の「インストール」から
- **iPhone (Safari)** — 共有ボタン →「ホーム画面に追加」

## デザイン

天球図（Celestial Chart）をモチーフにしています。

- 深いネイビー（`#0E1724`）とオフホワイトを基調に、真鍮色 / シャンパンゴールドの細線を控えめなアクセントとして使用
- 欧文は Cormorant Garamond、和文は Zen Old Mincho
- 星座線と星はインライン SVG で背景にごく薄く配置（装飾であり情報ではありません）
- 起動時に短いブランドイントロを表示し、メイン画面へクロスフェード
- `prefers-reduced-motion`、キーボード操作、`focus-visible` に対応

## データ

`filtered_data.json` が唯一のデータソースです。表示・検索・CSV はすべてこのファイルから生成されます。

| キー | 内容 |
| --- | --- |
| `menu` | 料理名 |
| `restaurant` | 店舗名 |
| `area` | エリア |
| `author` | 考案者 |
| `price` | 価格（円） |
| `coaster` | コースター種別（例: `ボイスA` / `謎B`） |
| `url` | 店舗ページ URL |
| `is_closed` | 閉店フラグ（`true` = 閉店） |

閉店フラグは `check_urls.py` で更新します。各店舗ページに実際にアクセスし、404 または閉店案内が返る店舗を `is_closed: true` として `filtered_data.json` を書き出します。

```bash
python check_urls.py
```

（`requests` と `beautifulsoup4` が必要です）

## ファイル構成

```
index.html           メイン HTML（CSS / JS 同梱、filtered_data.json を読み込む）
filtered_data.json   メニューデータ
manifest.json        PWA マニフェスト
service-worker.js    オフラインキャッシュ
icon.svg / icon-*.png  アプリアイコン
check_urls.py        閉店店舗チェック（filtered_data.json を生成）
resize_icon.py       PWA アイコン生成
update_html.py       旧版のデータ埋め込みスクリプト（現在は未使用）
```

フレームワーク・ビルド工程はありません。静的ファイルをそのまま配信しています（GitHub Pages）。

## 注意事項

- 本サイトは非公式です。TDC（トーキョー・ディスカバリー・シティ）および株式会社 baton とは一切関係ありません
- データは [公式 FOOD ページ](https://tokyo-discovery-city.quizknock.com/food/) を参照して作成しています
- データの著作権は各権利者に帰属します

## Thanks

- QuizKnock、TDC 運営チーム
- [@heki-dm](https://github.com/heki-dm) — コードのリファクタリングに協力
