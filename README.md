# my-gentoo-custom
## 需要安装:
### 字体
* media-fonts/wqy-microhei  
* ttf-ubuntu-font-family
### i3wm 组件
* i3blocks
* i3lock
* ranger
### 壁纸
* feh
### 透明化
* Compton
### 输入法
* app-i18n/fcitx
* app-i18n/fcitx-configtool
* app-i18n/fcitx-sunpinyin
* xautolock
### 常见问题
#### burpsuite 锯齿字体问题
* 修改 /usr/bin/burpsuite   
`java -jar /opt/burpsuite/burpsuite_community_v1.7.36.jar >/dev/null 2>&1 &`   
`java -jar` ***-Dawt.useSystemAAFontSettings=on*** `/opt/burpsuite/burpsuite_community_v1.7.36.jar >/dev/null 2>&1 &`
#### HDMI ALSA +PulseAudio 配置
* 录音设备默认有*标记
 `$ pacmd list-sources | grep -e 'index:' -e device.string -e 'name:'` 
* 播放设备默认有*标记
 `$ pacmd list-sinks | grep -e 'name:' -e 'index:'`
* 改变默认播放设备
修改/etc/pulse/default.pa 以下是我自己的hdmi声音设备   
`
...
set-default-source alsa_output.pci-0000_02_00.1.hdmi-stereo.monitor
...
`   
#### 休眠
在i3config 中配置 `xautolock -time 30 -locker "sudo pm-suspend" &`
