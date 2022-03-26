# Install iterm2  

### 安裝 iterm2
在 Terminal 下以下指令，直接透過 Homebrew 安裝  
`$ brew cask install iterm2`  

### 安裝 ZSH  
ZSH 是用來取代 BASH 的一種工具  

下以下指令安裝  
`$ brew install zsh zsh-completions`  

確認一下是否安裝完成  
`$ zsh --version`  

接下來將終端機預設改成 ZSH  
`$ sudo sh -c "echo $(which zsh) >> /etc/shells"`  
`$ chsh -s $(which zsh)`  

確認修改完成  
將 Terminal 關掉重開以後輸入以下指令  
`$ echo $SHELL`  

如果有修改成功的話應該會看到 **/usr/local/bin/zsh**  

## 更新版
**安裝順序： iTerm2 -> Oh My Zsh**
  
### 安裝 iTerm2
使用 Homebrew 安裝
```shell
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
```shell
$ brew cask install iterm2
```

### 選擇配色主題
到下方網址下載主題並解壓縮  
[iTerm2 配色主題](https://iterm2colorschemes.com/)
  
#### 打開 iTerm2
找到剛剛下載的主題 import 到列表裡，再點選一次 Color Presets 選取剛剛 import 主題
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

### 安裝 oh-my-zsh
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