# Python Music player 使用 Termux + Python 建構非Android SDK Based 音樂播放器App

## 動機

當我們在使用電腦時，如果需要播放音樂，則我們會開啟一個網頁，在後台播放音樂。而如果我們在手機上要在背景播放音樂的話，當瀏覽器處於後台進程時，他會被暫停；而如果使用Youtube，則需要Youtube Premium才支持。因此我想著使用我熟悉的Python製作一個音樂播放程式。

## 參考

## 計劃、執行流程

1. VLC Library 播放功能基本實現
2. 暫停，播放功能實現
3. 單曲循環，清單循環功能實現
4. 跳過，清空功能實現
5. 播放網路資源，搜索歌曲功能實現
6. 使用Termux執行

## 成果簡介

> 項目開源地址：[Github](https://github.com/iceice666/kusa.player.python)

（插入執行的截圖

* 播放、暫停
* 迴圈
* 歌曲查詢、點播
* 歌單的儲存與播放

## 反思與心得

目前這個階段，基本的功能都已經實現，命令行的交互也趨於完善，不過如果在手機上，另外實作一個UI效果會比較好，或是移植到Android，使用Android SDK實作；而如果要在ios上執行，則需要改用objective-c或swift來進行開發。

而這個項目呢，有一個[Discord Bot](https://github.com/iceice666/DiscordBot)的前身，不過兩個項目的實現方式不同：Discord Bot是透過把video stream（視訊流）轉成audio stream （音訊流）推送到官方的API，用戶和bot在同一個語音頻道收聽。

而相對於前一個項目有官方API，這一個項目是需要從0開始自己適配各種系統（像如果用Termux，控制音量的功能就無法使用，可能是因為VLC的api和Android API衝突）。

（個人認為）能真正解決跨平台問題是使用Java開發或是改成單一網頁（不過這又回到了一個問題，就是我為啥不要直接用網頁播放呢，可能到後來的優勢只剩下可不斷擴充的來源API 。）
