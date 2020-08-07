# 簡易網頁程式 (以 Windows 為例)
## 假設我們是負責佈署 (程式運行) 環境的工程師
### 建立簡易網頁程式的執行環境
  * 下載並安裝 Anaconda 64-Bit Graphical Installer
  * 在 「開始」中找到並執行 Anaconda Prompt (Anaconda3)
  * `conda create -n simple-full-stack python=3`建立新 Python 環境
  * `conda activate simple-full-stack`進入新環境
  * `conda install -y flask`安裝額外的 Python 套件
### 下載簡易網頁程式
  * `git clone https://github.com/quakelai/simple-full-stack.git`
  * 網頁程式經常區分為前後端。本程式的 templates/index.html 為前端，app.py 為後端
    * 什麼是前端？什麼是後端？ https://15days.website/posts/frontend-vs-backend
  * templates/index.html 模擬了資料庫的基本功能 (CRUD: Create, Read, Update, & Delete)，因此本程式未使用真正的資料庫
### 程式運作流程大致為：使用者 > 瀏覽器 > 網域 > SSL憑證 (https) > Public IP > 前端程式 > 後端程式 > 資料庫。佈署環境時，要處理「網域 >>>>> 資料庫」這一段。
### 執行簡易網頁程式
  * `cd simple-full-stack`進入 simple-full-stack 目錄
  * `python app.py`執行程式
  * 如執行成功，可在瀏覽器上透過本機位址使用程式 (http://127.0.0.1:5000 或 http://localhost:5000)
### 以 ngrok 程式快速處理「網域 > SSL憑證 (https) > Public IP」這一段工作
  * 下載並解壓縮 ngrok 程式
  * 再開一個 Anaconda Prompt (Anaconda3)
  * 移動至 ngrok 程式所在目錄並執行
    * `cd Downloads`進入 Downloads 目錄
    * `cd ngrok-stable-windows-amd64`進入 ngrok-stable-windows-amd64 目錄
    * `ngrok http 5000`執行 ngrok 程式
  * 如執行成功，會看到一段 https 網址如 https://cdcd5e0b3881.ngrok.io ，即可於任何一台機器的瀏覽器上，透過此網址使用程式
### 完成👍
### 參考資料
  * https://www.encodedna.com/javascript/how-to-create-a-simple-crud-application-using-only-javascript.htm
