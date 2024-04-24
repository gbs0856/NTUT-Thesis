# NTUT-Thesis
國立臺北科技大學碩博士論文XeLaTeX模板 (中英文皆支援)

## 軟體安裝(for windows)
依序安裝以下軟體(64bit):

1. Miktex Compiler - Latex的編譯器
   - https://miktex.org/download
   - 安裝過程中會詢問如果編譯期間缺少套件是否自動下載安裝，請選Yes

2. Ghostscript AGPL Release - 轉譯輸出成PDF必要轉譯器
   - https://www.ghostscript.com/download/gsdnld.html

3. GSView 6.0 Beta - 閱讀器，支援 Postscript, EPS, PDF, XPS, EPUB (version 2, no DRM), CBZ, JPEG, and PNG files
   - http://www.gsview.com/

4. TeXstudio - Latex文件編輯器
   - https://www.texstudio.org/

TeXstudio基本設定 Options -> Configure TeXstudio
 - General -> Language = "en"
 - Language Checking -> Default Language = "en_US" 
 - Editor -> Font Size -> 設定自己覺得舒服的大小(建議16)
 - Editor -> Font Encoding = "UTF-8"
 - 進階設定(Show Advanced Options) -> Adv. Editor -> Appearence -> Show line numbers = "All Line Numbers" (方便debug)

## 編譯相關說明
For Windows:
1. 因論文Dissertation.tex中引用了很多套件\usepackage(套件名)，缺少套件會無法編譯，
請先從windows開始列中找到MikTeX 2.9 -> Miktex Package Manager (Admin) 執行，
將所有用到的套件用名稱一一搜尋後右鍵安裝

2. TeXstudio無法編譯北科大碩博士論文時的設定，TeXstudio只當編輯器使用
   請執行資料夾中的make.bat進行編譯，可用文字編輯器修改make.bat中的命令(注意引號別刪)

3. TeXstudio編譯北科大碩博士論文時的設定 Options -> Configure TeXstudio -> Build 
 - Build & View = "Build & View"
 - Default Compiler = XeLaTex

For Overleaf:
1. 2024.04 已更新支援Overleaf

## 檔案說明

預設Main_Dissertation.tex為主檔，類似於開發程式時的Main Class/Main Function:

- Main_Dissertation.tex = 論文章節結構主檔
- FrontCover.tex = 封面
- InnerCover.tex = 內書頁
- Sign.pdf = 口試審定書PDF檔 //定稿時才插入 // 初稿時請先註解229~232行
- Acknowledgment.tex = 致謝
- Abstract_chinese.tex = 中文摘要 
- Abstract_en.tex = 英文摘要 
- reference.bib = 參考文獻原始清單
- Symbols.tex = 符號表 //放在論文最後
- background.png = 浮水印(北科大校徽)
- Logo.png = 封面LOGO(北科大校徽)

其他檔案自行照章節改名與修改主檔內容插入

## 格式上的注意事項

1. 若是要單面印刷，請將Dissertation.tex檔案中\newblankpage命令加上"%"註解掉或刪除，
出現\chapterfinished命令，請註解掉改成\clearpage

2. 預設輸出的論文為包含電子書籤(bookmarks)之版本，使用電腦與平板閱讀方便，
   若要輸出紙本列印使用(無電子書籤版)，請依照以下步驟執行
   1.	請先以預設版本執行過一次make.bat檔
   2.	將Dissertation.tex檔案中第200~203行註解掉
   3.	再執行make.bat檔編譯一次

4. 無書籤版輸出是初稿紙本、定稿紙本、以及離校繳交檔案給圖書館用

## Latex參考資源
1. http://timshan.wikidot.com/latex-resources

## 一些廢話
2017年畢業時自己刻了這個template，想不到都已經2024年了，還有學弟妹們在網路上求Template，因此放上來造福學弟妹們。
