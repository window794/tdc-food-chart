# TDC FOOD CHART ／ 探る昼とめぐる夜

> フードを、星図から探す。
> トーキョー・ディスカバリー・シティ「探る昼とめぐる夜」コラボフード検索サイト（非公式）

[![Stars](https://img.shields.io/github/stars/window794/tdc-food-chart?style=for-the-badge&color=D4AF37&labelColor=131d2a)](https://github.com/window794/tdc-food-chart/stargazers) [![Forks](https://img.shields.io/github/forks/window794/tdc-food-chart?style=for-the-badge&color=4a90d9&labelColor=131d2a)](https://github.com/window794/tdc-food-chartforks) [![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-222?style=for-the-badge&logo=github&logoColor=white&labelColor=131d2a)](https://window794.github.io/tdc-food-chart/) [![PWA](https://img.shields.io/badge/PWA-Ready-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white&labelColor=131d2a)](https://window794.github.io/tdc-food-chart/) [![Menus](https://img.shields.io/badge/収録メニュー-40件-D4AF37?style=for-the-badge&labelColor=131d2a)](https://window794.github.io/tdc-food-chart/) [![Unofficial](https://img.shields.io/badge/Fan%20Made-Unofficial-ff69b4?style=for-the-badge&labelColor=131d2a)](https://github.com/window794/tdc-food-chart)

天球図（Celestial Chart）をモチーフにした、QuizKnockコラボメニューの検索サイトです。

## 🌐 サイトURL
**👉 https://window794.github.io/tdc-food-chart/**

---

## 技術スタック

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

## ホスティング

![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222?style=for-the-badge&logo=github&logoColor=white)

---

## 🌟 特徴

### 🎨 デザイン — 天球図 / Celestial Chart
- **深いネイビー**（`#0E1724`）とオフホワイトの静かな配色
- **真鍮色 / シャンパンゴールド**の細線による控えめなアクセント
- **明朝体フォント**（Cormorant Garamond + Zen Old Mincho）
- 背景と余白に**星座線と星**をごく薄く散らした装飾（インラインSVG）
- 起動時の**ブランドイントロ**（約2.9秒、メイン画面へ静かにクロスフェード）
- 結果タイルは**真鍮の線が静かに反応する**控えめなホバー
- `prefers-reduced-motion` 対応、キーボード操作・focus-visible 対応

### 🔍 機能
- **リアルタイム検索** - 入力すると即座にフィルタリング（メニュー・店舗・エリア・考案者・コースターを横断）
- **多彩な絞り込み** - コースター種別（ボイス / 謎 / クイズ）と A・B、エリア、店舗、考案者、価格帯
- **閉店店舗の扱い** - `is_closed` に基づく「閉店」表示。閉店店舗を含める／含めないを切り替え可能
- **柔軟な並び替え** - エリア順、価格順、メニュー名順、店舗名順、考案者順
- **詳細シート** - タイルをタップすると店舗ページへのリンク付きの詳細を表示
- **CSV出力** - 検索結果をダウンロード可能（BOM付きUTF-8）
- **📱 PWA対応** - インストールしてアプリとして使える！

---

## 🚀 PWAとして使う

このサイトは **PWA（Progressive Web App）** に対応しています！

### 📲 インストール方法

#### Chromeの場合
1. サイトを開く
2. アドレスバーの右側に表示される **「インストール」** ボタンをクリック
3. ホーム画面にアイコンが追加されます！

#### iPhoneの場合
1. Safariでサイトを開く
2. 画面下部の **共有ボタン** をタップ
3. **「ホーム画面に追加」** を選択
4. アプリとして使えます！

### ✨ PWAのメリット
- 📱 **アプリのように使える** - ホーム画面から起動
- ⚡ **高速起動** - キャッシュで素早く表示
- 🔌 **オフライン対応** - ネットがなくても動作（データは最終アクセス時のもの）

---

## 📊 データについて

### 収録メニュー数
**全40件** のコラボメニューを収録！

### データの内訳
- **エリア**: ラクーア DELI & DISH、ラクーア、スパ ラクーア、東京ドームシティ アトラクションズ、東京ドームホテル、FOOD STADIUM TOKYO、Space Travelium TeNQ
- **考案者**: 伊沢拓司、須貝駿貴、ふくらP、河村拓哉、山本祥彰、鶴崎修功、東言、東問
- **価格帯**: ¥630〜¥2,500
- **コースター種類**: ボイスA/B、謎A/B、クイズA/B

---

### 使用フォント
- **Cormorant Garamond** - ブランド名・価格・件数・ラベル（欧文）
- **Zen Old Mincho** - 本文すべて（和文）

---

## 📁 ファイル構成

```
📦 TDC FOOD CHART
├── 🌐 index.html                     - メインHTML（filtered_data.json を読み込んで表示）
├── 📊 filtered_data.json             - メニューデータ（閉店フラグ is_closed 付き）
├── 📋 manifest.json                  - PWA設定
├── ⚙️ service-worker.js              - オフライン対応
├── 🎨 icon.svg                       - アプリアイコン
├── 🌟 celestial-chart.png            - 星座盤画像
├── 🐍 check_urls.py                  - 閉店店舗チェックスクリプト（filtered_data.json を生成）
├── 🔄 update_html.py                 - 旧版のデータ埋め込みスクリプト（現在は未使用）
├── 🖼️ resize_icon.py                 - PWAアイコン生成
└── 📖 README.md                      - このファイル
```

---

## 💡 使い方

### 🔎 基本的な検索
1. **キーワード** に好きな言葉を入力（例: "いちご"、"クレープ"）
2. 結果が**リアルタイム**で絞り込まれます

### 🎯 詳細な絞り込み
- **考案者で絞る** - 好きなQuizKnockメンバーのメニューだけ表示
- **エリアで絞る** - 行く場所に合わせて検索
- **価格で絞る** - 予算に合わせた検索
- **コースターで絞る** - 欲しいコースターの種類で検索

### 💾 データの保存
- **CSV出力ボタン** で検索結果をダウンロード
- Excelで開いて管理できます

---

## 🎨 デザインのこだわり

### 🌌 配色
| 色 | 用途 | カラーコード |
|---|---|---|
| 🌃 ディープネイビー | 背景・カード | `#0E1724` |
| 🌊 ネイビー（明） | カードのhover / 詳細シート | `#131E2E` / `#101C2B` |
| 🕯 真鍮 | 細線・小さなアクセント | `#A88B5C` |
| ✨ シャンパンゴールド | 価格・件数・リンク | `#D8C69E` |
| 💫 オフホワイト | 本文・見出し | `#EEF1F5` / `#F2EFE8` |
| 🎨 グレイブルー | 補助テキスト | `#9AA7B8` |

### ✨ モーション
- **ブランドイントロ** - 星と星座線が静かに現れ、タイトルがぼやけた状態から鮮明になり、メイン画面へクロスフェード
- **カードのhover** - 真鍮色の細線と、ごくわずかな背景の明るさの変化のみ（発光や大きな移動はしない）
- **prefers-reduced-motion** - すべてのアニメーションを短絡

---

## 📝 注意事項

⚠️ **このサイトは非公式です**
- TDC（トーキョー・ディスカバリー・シティ）や株式会社batonとは一切関係ありません
- ファンが作成した非公式の検索ツールです
- データは公式サイトを参照していますが、最新情報は[公式FOOD ページ](https://tokyo-discovery-city.quizknock.com/food/)でご確認ください

🎫 **コラボは終了しています**
- このコラボは既に終了しています
- 記録・アーカイブとしてご利用ください

---

## 🤝 貢献

バグ報告や機能提案は大歓迎です！

---

## 📜 ライセンス

このプロジェクトは個人的な非公式ツールです。  
データの著作権は各権利者に帰属します。

---

## 🌟 Special Thanks

- **QuizKnock** - 素敵なコラボメニューをありがとうございました
- **TDC運営チーム** - 楽しいイベントをありがとうございました
- **[@heki-dm](https://github.com/heki-dm)** - コードのリファクタリングにご協力いただきました
- **すべての訪問者** - 使ってくれてありがとうございます！

---

<div align="center">

### ✨ Made with 💛 for QuizKnock Fans

**フードを、星図から探す。**

---

🔗 [公式TDC FOODページ](https://tokyo-discovery-city.quizknock.com/food/)

</div>
