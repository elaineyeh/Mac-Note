# Install iterm2  
**安裝順序： iTerm2 -> ZSH -> Oh My Zsh**
### 安裝 iTerm2
安裝 Homebrew
```shell
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
使用 brew 安裝 iTerm2
```shell
$ brew install --cask iterm2
```

### iTerm2 選擇配色主題
到下方網址下載主題並解壓縮  
[iTerm2 配色主題](https://iterm2colorschemes.com/)

#### 打開 iTerm2
找到剛剛下載的主題 import 到列表裡，再點選一次 Color Presets 選取剛剛 import 主題  
下載配色主題檔案路徑
```
repo > schemes > 所有主題
```
iTerm2 匯入地方
```
Preferences > Profile > Colors > 右下角 Color Presets > import
```
  
### 選擇字型
有些主題會用到一些特殊 icon，所以 iTerm2 選用的字型必需要支援這種特殊 icon font
```shell
$ git clone git://github.com/powerline/fonts ~/.powerline_fonts
```
```shell
$ cd ~/.powerline_fonts
```
```shell
$ ./install.sh
```

#### 打開 iTerm2
```
Preferences >Profile > Text > Change Font
```

### 安裝 ZSH  
ZSH 是用來取代 BASH 的一種工具  

下以下指令安裝  
```shell
$ brew install zsh zsh-completions
```  

確認一下是否安裝完成  
```shell
$ zsh --version
```  

接下來將終端機預設改成 ZSH  
```shell
$ sudo sh -c "echo $(which zsh) >> /etc/shells" 
$ chsh -s $(which zsh)
```  

確認修改完成  
將 Terminal 關掉重開以後輸入以下指令  
```shell
$ echo $SHELL
```  

如果有修改成功的話應該會看到 **/usr/local/bin/zsh**  
(但現在 M1 以後預設就是 zsh 所以路徑會稍有不同)

### 安裝 oh-my-zsh
Oh My Zsh 是一個用來管理 ZSH 設定檔（configuration）的框架，提供了很多的外掛（plugin）和主題（theme）可以選擇。
```shell
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
[oh-my-zsh Theme](https://github.com/robbyrussell/oh-my-zsh/wiki/themes) 有很多主題，選喜歡的之後輸入指令
```shell
$ vim ~/.zshrc
```
將主題改成自己喜歡的並存擋
```
ZSH_THEME="THEME_YOU_LIKE"
```
並讓修改過的 zsh 生效
```shell
$ exec $SHELL
```

## Reference
[Mac終端機 (Terminal)設定： iTerm 2](https://medium.com/nitas-learning-journey/mac%E7%B5%82%E7%AB%AF%E6%A9%9F-terminal-%E8%A8%AD%E5%AE%9A-iterm2-ba63efd0df6a)  
[為 MAC 的 Terminal 上色 - 透過 iTerm 2 和 Oh My Zsh 高亮你的終端機](https://pjchender.dev/app/mac-terminal-iterm2/)