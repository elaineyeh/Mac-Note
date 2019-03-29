# Install iterm2  

## 安裝 iterm2
在 Terminal 下以下指令，直接透過 Homebrew 安裝  
`brew cask install iterm2`  

## 安裝 ZSH  
ZSH 是用來取代 BASH 的一種工具  

下以下指令安裝  
`brew install zsh zsh-completions`  

確認一下是否安裝完成  
`zsh --version`  

接下來將終端機預設改成 ZSH  
`sudo sh -c "echo $(which zsh) >> /etc/shells"`  
`chsh -s $(which zsh)`  

確認修改完成  
將 Terminal 關掉重開以後輸入以下指令  
`echo $SHELL`  

如果有修改成功的話應該會看到 **/usr/local/bin/zsh**  