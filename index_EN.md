# Multiple Launcher
[English Version](index_EN.md) | [GitHub](https://github.com/stakiran/multiple_launcher/)

## Summary
- Create an .ahk file that lists multiple files and URLs to open
    - This is called a Multiple Launcher
- If you prepare a Multiple Launcher in advance, you can open everything at once just by launching it when needed

## Requirements
- Windows
- AutoHotkey

## Sample
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

When you run L1.ahk, all listed files and URLs will be opened.

## Typical times to use it
- Things to use at startup
- Things you want to see first thing in the morning
- Things you want to see when starting work
- Things you want to see when starting Project X

## Tips
- Because it's called a "launcher," you might imagine "programs," but it can be used for other things too
    - Text files containing notes or templates
    - Pages for some SaaS
- On Windows, associated files can be opened by specifying just the file path
    - This approach works well for text files and URLs
- For items you no longer use, set them aside by commenting them out with `;`
    - You may revisit or reuse them later, so it often feels better to keep them as comments rather than deleting them outright