# my-gentoo-custom
## 需要安装:
### 字体
* media-fonts/wqy-microhei  
* ttf-ubuntu-font-family
### i3wm 组件
* i3blocks
* i3lock
### 壁纸
* feh
### 透明化
* Compton
### 输入法
* app-i18n/fcitx
* app-i18n/fcitx-configtool
* app-i18n/fcitx-sunpinyin

### burpsuite 锯齿字体问题
* 修改 /usr/bin/burpsuite 
  java -jar /opt/burpsuite/burpsuite_community_v1.7.36.jar >/dev/null 2>&1 &
  java -jar -Dawt.useSystemAAFontSettings=on /opt/burpsuite/burpsuite_community_v1.7.36.jar >/dev/null 2>&1 &


