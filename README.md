# 簡易網頁程式
## 假設我們是負責部署(程式運行)環境的工程師
### 安裝後端程式的語言 (Python) 的執行環境，以 Windows 為例
  * 下載並安裝 Anaconda(Python) 64-Bit Graphical Installer
  * 在 "開始" 中找到並執行 Anaconda Prompt (Anaconda3)
  * `conda create -n simple-full-stack python=3` 建立新 Python 環境
  * `conda activate simple-full-stack` 進入新環境
  * `conda install -y flask` 安裝額外的 Python 套件
### 下載全端網頁程式
  * `git clone https://github.com/quakelai/simple-full-stack.git`
  * app.py 由後端工程師提供；templates/index.html 由前端工程師提供
  * templates/index.html 已包含基本資料庫功能 (CRUD: create, read, update, & delete)
### 一般，資料庫由資料庫管理員或後端工程師提供，與後端程式串接
### 程式使用流程大致為：使用者 > 瀏覽器 > 網域 > SSL憑證 (https) > Public IP > 前端程式 > 後端程式 > 資料庫
### 執行程式
  * `cd simple-full-stack`
  * `python app.py`
  * 程式已運行，可在劉覽器上透過本機位址使用 (http://127.0.0.1:5000 或 http://localhost:5000)
### 以 ngrok 程式處理 "網域 > SSL憑證 (https) > Public IP" 這一段工作
  * 搜尋 "ngrok download"，下載並解壓縮 ngrok 執行檔
  * 再開一個 Anaconda Prompt (Anaconda3)
  * 移動至 ngrok 執行檔所在目錄，如
    * `cd Downloads`
    * `cd ngrok-stable-windows-amd64`
  * 執行`ngrok http 5000`後，會看到一段 https 網址如`https://cdcd5e0b3881.ngrok.io`，可於任何一台機器的瀏覽器上，透過此網址使用程式
### 完成～
