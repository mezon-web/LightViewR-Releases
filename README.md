<img src="assets/LightViewR.png" width="64" alt="LightViewR アイコン">

# LightViewR 📄

Windows向けの、軽快なPDF・Markdown・テキスト・表・HTMLビューワです。

**[LightViewR v0.3.11 をダウンロード](https://github.com/mezon-web/LightViewR-Releases/releases/tag/v0.3.11)**

v0.3.9からアプリ名とEXE名をLightViewRに統一しました。過去のリリースと添付ZIPは当時の名前で残しています。

v0.3.10では検索の塗りを薄くし、検索語のクリアと、本文をクリックした位置からの検索移動に対応しました。

v0.3.11ではPDFのページ番号の左右にある前後ページボタンを見やすくしました。

設定・履歴・読書位置は、起動後にEXE横へ作成される `UserData` に保存します。[長いPDFの表示例](assets/scrollbar-0.3.4.png)も確認できます。

## はじめに

1. 正式版のリリースページの **Assets** から `LightViewR-v0.3.11.zip` をダウンロードします。
2. ZIPを展開し、`LightViewR-v0.3.11` フォルダ内の **LightViewR.exe** を起動します。
3. 「開く」またはファイルのドラッグ＆ドロップで文書を開きます。

インストーラーはありません。フォルダごと保存して使うポータブル版です。
展開した `LightViewR-v0.3.11` フォルダの **LightViewR.exe** を起動し、補助フォルダ **_support** はEXEと一緒に保存してください。起動後に個人設定用の **UserData** が作成されます。
使い方は右端の **「？」／F1** または [操作説明](docs/操作説明.md) で確認できます。

## 必要な実行環境

- **Windows x64** と **.NET 10 Desktop Runtime x64**。導入済みなら追加のインストールは不要です。[Microsoft公式ダウンロード](https://dotnet.microsoft.com/ja-jp/download/dotnet/10.0) の「.NET デスクトップ ランタイム」から取得できます。
- **Markdown・HTMLの表示**にはMicrosoft Edge WebView2 Runtimeが必要です。[Microsoft公式ページ](https://developer.microsoft.com/ja-jp/microsoft-edge/webview2/) から取得できます。未導入の場合はアプリ内で導入先と再試行を案内します。

.NETとWebView2 RuntimeはZIPに同梱していません。PDF・TXT・LOG・CSV・TSV・JSON・XML・INIの利用ではWebView2を起動しません。

## 対応形式と主な機能

| 形式 | 主な機能 |
| --- | --- |
| PDF | 連続スクロール、ページ移動、文字選択・コピー、検索、しおり目次、文書内リンク |
| Markdown | 表、コードの色分け・コピー、ローカル画像、Mermaid、数式、見出し目次 |
| TXT・LOG | 行番号、検索・コピー、大きな文書の仮想化表示、LOGの追記追従 |
| CSV・TSV | 表表示、見出し固定、列幅変更、全セル検索、セルコピー、絞り込み・並べ替え |
| JSON・XML・INI | 色分け、文字コード選択、折り返し、検索・コピー |
| HTML | ローカルの静的HTML、見出し目次、検索・コピー |

全形式でファイル履歴、拡大縮小、検索結果の一覧、読書位置の復元、戻る／進むを利用できます。PDF以外は保存時の自動更新とF5更新に対応し、複数の文書は別ウィンドウで開きます。

対応する斜めのテキスト透かしがあるPDFでは「斜め透かしを非表示」を利用できます。Windows標準OCRが利用できる環境では、画像PDFの現在のページや指定範囲を認識して検索・コピーできます。元のPDFファイルは変更しません。

「検索」は「目次」の右にあります。画面幅に収まらない操作は「…」に入り、ウィンドウを広げるとボタンへ戻ります。

右上の太陽／月でライト／ダークを切り替えられます。設定は再起動後も復元し、PDFの紙面は元の色を保ちます。

Markdown・HTMLの埋め込みスクリプトを実行せず、外部画像を自動取得しません。閲覧専用です。

## 画面

検索欄内の×で検索語をクリアできます。右端の×は検索欄を閉じます。

![検索語のクリア](assets/search-0.3.10.png)

![PDF検索画面：ライトとダーク](assets/compare-search-0.3.3-design.1.png)

![Markdown画面：ライトとダーク](assets/compare-markdown-0.3.3-design.1.png)

![PDF表示例](assets/viewer.png)

![アプリ内ヘルプ](assets/help.png)

## 更新と確認

アプリを終了し、新しいZIPを別フォルダへ展開してください。旧版の起動フォルダに **UserData** がある場合は、新しい `LightViewR.exe` と同じ場所へコピーすると履歴・読書位置・外観設定を引き継げます。旧版のLocalAppDataにある設定は自動移行しません。設定の保存には展開先への書き込み権限が必要です。
各リリースにZIPの **SHA-256チェックサム** を添付しています。

Windows 11 x64向けです。Windows 10実機では未確認です。追記読込や大きな文書の初回表示は、全体照合とCSVの構造検査により時間がかかる場合があります。大きな文書の一時保持には元ファイル相当のディスク空きが必要です。
[変更履歴](CHANGELOG.md) / [第三者ソフトウェアの表記](THIRD-PARTY-NOTICES.md)

このリポジトリは配布版と利用者向け文書を管理します。第三者ソフトウェアのライセンスは配布ZIP内の `_support/licenses` フォルダに同梱しています。

リリースに自動表示される「Source code」は、この配布リポジトリの説明書・画像のアーカイブです。アプリ本体は、上記の正式版ZIPから入手してください。
