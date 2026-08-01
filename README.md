# 猫の暦 — 2026年8月

六曜・十二直・干支・九星・マヤ暦（Kin）・七十二候・吉日凶日をまとめた開運カレンダー。日ごとのテーマと「最適な行動 / 注意する行動 / 開運フード / 吉方位 / 開運色 / 言霊」が付きます。

ホーム画面に追加すると、猫アイコンのアプリとして全画面で開き、電波がなくても使えます。

## 公開URL

**https://itaocomcom2-cyber.github.io/neko-koyomi/**

<img src="./qr.png" alt="公開URLのQRコード" width="200">

スマホのカメラでこのQRコードを読み取ると開きます。ログインは不要です。

## ホーム画面への追加

- **iPhone（Safari）** — ページを開く → 共有ボタン → 「ホーム画面に追加」
- **Android（Chrome）** — ページを開く → 右上メニュー → 「ホーム画面に追加」、または画面上部の「アプリに追加」ボタン

## ファイル構成

| ファイル | 役割 |
| --- | --- |
| `index.html` | カレンダー本体。暦データ・アドバイス・QRコード生成をすべて含む単一ファイル |
| `manifest.webmanifest` | アプリ名・アイコン・全画面表示の設定 |
| `sw.js` | オフラインで開くためのキャッシュ（Service Worker） |
| `icons/` | 猫アイコン（192 / 512 / マスカブル512 / Apple用180） |

## 更新するとき

`index.html` などを書き換えたら、**`sw.js` の `CACHE` の版数を上げてください**（例：`neko-koyomi-v1` → `neko-koyomi-v2`）。これを忘れると、追加済みのスマホで古い内容が表示され続けます。

```
git add -A
git commit -m "内容を更新"
git push
```

反映まで1〜2分かかります。

## 暦の出典と注意

日付の裏取りは [Magic Wands 開運カレンダー](https://www.magicwands.jp/calculator/calendar/?year=2026&month=8)、[一粒万倍日一覧](https://hana-yume.net/howto/ichiryumanbaibi/)、[国立天文台 令和8年暦要項](https://eco.mtk.nao.ac.jp/koyomi/yoko/2026/rekiyou262.html) によります。干支・六曜・十二直・九星・マヤ暦のKinは暦のルールに沿って計算し、複数の資料と照合しています。

一方、各日の「テーマ」「最適な行動」「注意する行動」「開運フード」「吉方位」「言霊」は、その日の暦を組み合わせた**解釈**です。

QRコードは外部サービスを使わず、`index.html` 内で生成しています。
