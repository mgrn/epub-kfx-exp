Kindle 顯示繁體中文
===================

測試電子文檔在 Kindle 上的顯示效果，以 EPUB 轉 KFX 為主。

所有文件出自「[台灣 EPUB 3 製作指引](https://github.com/dpublishing/epub3guide)」。

資料夾「zv」為「[直排文字書：羅生門](https://github.com/dpublishing/epub3guide/tree/master/practices/02_Reflow_Text_Vertical)」修改過後的版本，僅更動其中兩個檔案：
- `zv/item/standard.opf`
- `zv/item/style/style-standard.css`


生成 EPUB：
```
java -jar [指向epubcheck.jar路徑] zv -mode exp -save
```

或：
```
cd zv && zip -0Xq ../zv.epub mimetype && zip -Xr9Dq ../zv.epub * && cd ../
```

生成 KFX：
```
calibre-debug -r "KFX Output" -- zv.epub
```

其他說明：https://www.ptt.cc/bbs/book/M.1693849070.A.8BD.html
