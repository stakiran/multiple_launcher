# Multiple Launcher
[English Version](index_EN.md) | [GitHub](https://github.com/stakiran/multiple_launcher/)

## サマリー
- 複数のファイルや URL を開くよう記載した ahk ファイルをつくる
    - これを Multiple Launcher と呼ぶ
- Multiple Launcher をつくっておくと、必要なときにこれを開くだけで、一気に開ける

## 要件
- Windows
- 複数ファイルを開くポテンシャルを持つスクリプトシステム
    - AutoHotkey
    - バッチファイル

## サンプル1
L1.ahk として以下を保存。

```ahk
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

run,D:\github\stakiran\text\daily.md
run,D:\github\stakiran\text\home.trita
run,D:\github\stakiran\text\Personal_Roadmap.scb

run,https://keep.google.com/u/0/
run,D:\Dropbox\text\diary.md

run,"C:\Program Files (x86)\Mozilla Thunderbird\thunderbird.exe"

;run,D:\github\stakiran\text\home2.trita
;...
```

L1.ahk を実行すると、記述されたファイルや URL がすべて開かれる。

## サンプル2
バッチファイル xxx.bat として保存。

```bat
@echo off

echo chrome...
start "" "C:\Program Files\Google\Chrome\Application\chrome.exe"

echo text files...
start "" d:\dropbox\text\diary.txt
start "" d:\dropbox\tasks\today.md
```

ポイントは `start "" "CommandLine"` により起動すること。

## 主なタイミング
- 起動時に使うもの
- 朝一で見たいもの
- 仕事を始めるときに見たいもの
- プロジェクトXを始めるときに見たいもの

## TIPS
- ランチャーとあるから「プログラム」をイメージするが、それ以外もありえる
    - メモやテンプレートを書いたテキストファイル
    - 何らかの SaaS のページ
- Windows では関連付けられたファイルはファイルパス指定だけで開ける
    - テキストファイルや URL はこのやり方が良い
- 使わなくなったものはコメント `;` で退避しておく
    - 再検討や再利用時に使うことがあるので、消すよりはコメントで残しておいた方が良いと感じる
