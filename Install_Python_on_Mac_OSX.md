# How to install Python on Mac OSX

[Step1. 安裝 Xcode](#tag-xcode)

[Step2. 安裝套件管理 Homebrew](#two)

[Step3. 安裝 Python](#three)

[Step4. 設定路徑 $PATH](#four)

[Step5. 確認安裝](#five)

<h2 id="tag-xcode"> Step1. 安裝 Xcode </h2>
上 App Store 下載 Xcode

然後到 Terminal 輸入來安裝 Xcode command line tool  

下以下指令  
`xcode-select --install`  

<h2 id="two"> Step2. 安裝套件管理 Homebrew </h2>

下以下指令  
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```  

```
Press RETURN to continue or any other key to abort

請按 Enter
```  

安裝好後可以執行以下指令確認安裝完成  
`brew doctor`  

若出現 **Your system is ready to brew.** 則表示安裝完成  

<h2 id="three"> Step3. 安裝 Python </h2>
### 利用 Homebrew 搜尋 Python  
`brew search python`  

### 安裝 Python & Python3  

**Python**  
`brew install python`  

**Python3**  
`brew install python3`  

安裝的時候，Python 會被安裝在  **/usr/local/Cellar**  

打開資料夾  
`open /usr/local/Cellar`  

就可以看到剛剛安裝的 Python & Python3 了  

<h2 id="four"> Step4. 設定路徑 $PATH </h2>
路徑就是當你下指令時電腦知道要去哪裡找相關套件，而指令就是程式，他去幫你找"路徑"下有符合的第一個程式執行  

下以下指令  
`echo $PATH`  

會看到類似下列路徑  
`/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin`  

分號就是分隔的意思，所以當你在 terminal 裡面輸入 brew 時系統就會開始從 /usr/bin 找起，如果找不到就往下一個 /bin 去搜尋，以此類推  

因此為了避免跟系統本身的 Python 打架，我們要取得管理員權限用 emacs 編輯一下路徑  
`sudo emacs /etc/paths`   

把 /usr/local/bin 移到上面去  

```
control + k：把一行字剪下來

control + y：把字貼上

control + x + s：存檔

control + x + c：關掉 emacs
```  

一開始順序
![一開始](https://i.imgur.com/XKxuTaK.png)

修改後順序
![修改成](https://i.imgur.com/FOAmJzd.png)

重新開啟 Terminal 就好了  

<h2 id="five"> Step5. 確認安裝  </h2>
接下來確認是不是讀到我們安裝的 Python  
`which python`  

會看到 **/usr/local/bin/python**  

再看看 Python3  
`which python3` 

會看到 **/usr/local/bin/python3**  

## 完成以上步驟就代表安裝完成了
