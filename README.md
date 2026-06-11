# Bookmark Manager

![Tauri 2](https://img.shields.io/badge/Tauri-2-blue)
![Binary](https://img.shields.io/badge/binary-4.2MB-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

ポータブルで軽量なブックマーク編集ソフトです。
ブラウザ互換の HTML 形式でブックマークを管理し、インストール不要の単一 exe (約 4.2 MB) で動作します。

## ダウンロード
最新版は [Releasesページ](https://github.com/ユーザー名/リポジトリ名/releases) からダウンロードしてください。

## 特徴

- **インストール不要のポータブル設計**
  exe 単体で動作。データ (`bookmarks.html`)・設定 (`settings.json`)・アイコンキャッシュ (`icons/`) はすべて exe と同じフォルダに保存されます。レジストリや AppData は使用しません。
- **ブラウザ互換のデータ形式**
  Netscape ブックマーク形式 (HTML) を採用。Chrome / Edge / Firefox とのインポート / エクスポートに完全対応しています。
- **エクスプローラー様式の UI**
  左にフォルダツリー、右にリストビューを配置。ドラッグ＆ドロップで直感的に整理できます。
- **プライバシー配慮**
  ファビコンをローカルにキャッシュしますが、「アイコンを表示」を OFF にするとキャッシュを即座に全削除する機能を搭載しています。

## 使い方

`bookmark-manager.exe` を任意のフォルダに置いて起動するだけです。

### ツールバー
- **開く / 保存**: ブックマークファイルの読み込み・書き出し。
- **＋ ボタン**: ブックマークやフォルダの追加。
- **検索**: 名前・URL を全フォルダ横断で部分一致検索。
- **アイコンを表示**: アイコンの表示切替(OFF 時にキャッシュを全削除)。

### 操作
- **ダブルクリック**: ブックマークなら規定ブラウザで開く、フォルダなら展開。
- **ドラッグ & ドロップ**: フォルダ間移動や並び替え。並び順は HTML ファイルにそのまま保存されます。

## 注意事項

- 初回起動時、exe と同じフォルダに `bookmarks.html` などが作成されます。
- Windows の環境（セキュリティ設定等）により、警告が表示される場合がありますが、本ソフトはオープンソースであり、中身は GitHub 上で公開・確認可能です。


```powershell
cd src-tauri
cargo build --release
# 生成物: src-tauri\target\release\bookmark-manager.exe
