# Multiple Launcher
[English Version](index_EN.md) | [GitHub](https://github.com/stakiran/multiple_launcher/)

## Summary
- Create an ahk file that lists multiple files and URLs to open
    - This is called a Multiple Launcher
- If you have a Multiple Launcher ready, you can open everything at once just by running it when you need it

## Requirements
- Windows
- A scripting system capable of opening multiple files
    - AutoHotkey
    - Batch files

## Sample 1
Save the following as L1.ahk.

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

When you run L1.ahk, all the files and URLs listed in it will be opened.

## Sample 2
Save as a batch file xxx.bat.

```bat
@echo off

echo chrome...
start "" "C:\Program Files\Google\Chrome\Application\chrome.exe"

echo text files...
start "" d:\dropbox\text\diary.txt
start "" d:\dropbox\tasks\today.md
```

The key is to launch using `start "" "CommandLine"`.

## Common Use Cases
- Things to open at startup
- Things you want to see first thing in the morning
- Things you want to open when starting work
- Things you want to open when starting Project X

## TIPS
- Since it's called a launcher, you might imagine a "program," but it can be other things too
    - Text files containing notes or templates
    - Pages from some SaaS
- On Windows, files associated with an application can be opened just by specifying the file path
    - This approach works well for text files and URLs
- Comment out things you no longer use with `;` to keep them around
    - You may use them again when revisiting or reusing, so it feels better to keep them as comments rather than deleting them