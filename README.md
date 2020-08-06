# 簡易全端網頁程式 (for Windows)
## 假設我們是負責部署(程式運行)環境的工程師
### 安裝後端程式的語言 (Python) 的執行環境
  * 安裝 Anaconda(Python) 64-Bit Graphical Installer
  * 在"開始"中找到並執行 Anaconda Prompt (Anaconda3)
  * `conda create -n simple-full-stack python=3` 建立新 Python 環境
  * `conda activate simple-full-stack` 進入新環境
  * `conda install -y flask` 安裝額外的 Python 套件
### 下載全端網頁程式
  * `git clone https://github.com/quakelai/simple-full-stack.git`
  * app.py 由後端工程師提供；templates/index.html 由前端工程師提供
  * templates/index.html 已包含基本資料庫功能 (CRUD: create, read, update, & delete)
  * 一般，資料庫由資料庫管理員或後端工程師提供，與後端程式串接
  * 使用者 > 瀏覽器 > 前端程式 > 後端程式 > 資料庫
  
