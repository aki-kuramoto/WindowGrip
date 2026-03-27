# WindowGrip

WindowGrip adds a title bar and resizable edges to any window.

(Japanese later - 日本語部分は英語部分の続きにあります)

## Overview

In modern desktop applications, tabs and menus are often integrated into the title bar, which can reduce visibility and make window manipulation less intuitive.
"Window Grip" is a utility that overlays a classic (Windows 98/2000 style) "title bar (grip)" and "borders" around target windows, synchronizing their operations. This allows for easy and reliable window movement and resizing, just like in the good old days.

## System Requirements

- Windows 11 (x86-64)
- Windows 10 (x86-64)

## Key Features

- Top Grip Overlay: Drag the entire grip to move the target window. When the target window is moved, the grip automatically follows.
- Resize Borders: Displays borders on the remaining three sides, making it easy to resize windows that have thin, modern borders.
- Classic Window Controls (Windows 98/2000 style):
  - Top-Left Icon: Displays a menu; double-click the icon to close both the grip and the target window.
  - Top-Right Buttons: Standard Minimize, Maximize, and Close buttons.
- System Tray Integration: The application runs in the system tray (notification area). Right-click the tray icon to "Reload Config" or "Exit" the application.

## Installation & Recommended Usage

There is no installer. Simply extract the files to a folder of your choice and run `WindowGrip.exe`.

[Recommended Startup Setting]
To keep the application running continuously, we recommend adding it to your Windows Startup folder.
1. Type `shell:startup` into the Explorer address bar and press Enter.
2. Create a shortcut of `WindowGrip.exe` and place it in the opened "Startup" folder.

## Configuration File

Target window filtering and other settings are managed via a configuration file.

Location: 
%USERPROFILE%\.app-data\WindowGrip\window_grip_cfg.txt 

*If the file does not exist, it will be created automatically with default settings upon the first launch.

[Configuration Format]
```window_grip_cfg.txt
# Window Grip Configuration File
# Format: WindowClassName, ExecutableName, Include(true/false)
# Empty fields act as wildcards.
# Empty lines and lines starting with # are ignored.

# (Example) Default settings
ApplicationFrameWindow, applicationframehost.exe, false
, , true
```

*Note: You can reload the configuration file at any time by right-clicking the system tray icon and selecting "Reload Config".

# Uninstallation
This application does not use the Windows Registry. Simply delete the executable file and the configuration folder (`%USERPROFILE%\.app-data\WindowGrip\`).

# Licenses & Disclaimer
For terms of use (copyright, disclaimer, prohibitions, etc.), please refer to the included "LICENSE.txt".
For third-party library licenses, please see "third-party-notices.txt".

---

## Japanese Part
```Japanese-part.txt
=========================
 日本語
=========================

■ 概要
最近のデスクトップアプリは、タイトルバーにタブやメニューが統合されており、ウィンドウを移動させるための操作性や視認性が低下していることがあります。
「Window Grip」は、対象ウィンドウの周囲に昔ながらの (Windows 98 / 2000風の) 「タイトルバー (グリップ) 」と「枠 (縁) 」を外部からオーバーレイ表示し、操作を同期させるユーティリティです。
これにより、現代のアプリでも直感的なウィンドウの移動やサイズ変更が可能になります。

■ 動作環境
- Windows 11 (x86-64 環境) 
- Windows 10 (x86-64 環境) 
※上記にて動作確認済みです。

■ 主な機能
- ウィンドウ上部へのグリップ表示: グリップ全体をドラッグすることで、対象ウィンドウを移動できます。ウィンドウ側を移動させた場合もグリップが追従します。
- リサイズ枠の追加: 残りの三辺にも「縁」を表示し、最近のリサイズしづらい細い枠のウィンドウも、昔のように簡単にサイズ変更が可能です。
- クラシックなウィンドウ操作 (Windows 98/2000 風):
  - 左上アイコン: クリックでメニュー表示、ダブルクリックでグリップおよび対象ウィンドウを閉じます。
  - 右上ボタン: 最小化、最大化、閉じる操作が可能です。
- タスクトレイ常駐機能: 本ソフトはタスクトレイ (通知領域) に常駐します。アイコンを右クリックすることで、設定ファイルのリロードやアプリの終了が可能です。

■ インストール・おすすめの使い方
本ソフトウェアにインストーラーはありません。任意のフォルダに展開し、実行ファイル (WindowGrip.exe) を起動してください。

【おすすめの自動起動設定】
常に動作させておきたい場合は、Windowsのスタートアップに登録することをおすすめします。

1. エクスプローラーのアドレスバーに「shell:startup」と入力し、Enterキーを押します。
2. 開いた「スタートアップ」フォルダの中に、本ソフトの実行ファイルの「ショートカット」を作成・配置してください。

■ 設定ファイルについて
対象とするウィンドウのフィルタリングなどの設定は、以下の設定ファイルで行います。

保存場所: 
%USERPROFILE%\.app-data\WindowGrip\window_grip_cfg.txt 
※初回起動時に、ファイルが存在しない場合は自動的にデフォルト設定で作成されます。

【設定ファイルの書式】
--- window_grip_cfg.txt
# Window Grip Configuration File
# Format: WindowClassName, ExecutableName, Include(true/false)
# Empty fields act as wildcards.
# Empty lines and lines starting with # are ignored.

# (Example) Default settings
ApplicationFrameWindow, applicationframehost.exe, false
, , true
--- 

※ 空のフィールドはワイルドカード (すべてに一致) として機能します。
※ 設定ファイルを書き換えた後は、タスクトレイのアイコンを右クリックし「Reload Config (設定のリロード)」を選択することで即座に反映されます。

■ アンインストール
レジストリは使用していません。設定ファイルの入ったフォルダ (%USERPROFILE%\.app-data\WindowGrip\) と、本体のファイルを削除するだけで完了します。

■ ライセンス・免責事項
本ソフトウェアの利用規約 (著作権、免責事項、禁止事項など) については、同梱の「LICENSE.txt」をご確認ください。
また、使用しているサードパーティ製ライブラリのライセンスについては「third-party-notices.txt」をご参照ください。

========================================================================
Window Grip v2026.03.27
Copyright (c) 2026- Akihiro Kuramoto

GitHub: https://github.com/aki-kuramoto
Twitter: https://twitter.com/aki_kuramoto
========================================================================
```
