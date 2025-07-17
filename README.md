# 视频字幕AI自动识别显示工具
本项目是参考[openkylin-video]（https://github.com/UbuntuKylin/kylin-video），在其基础上进行视频字幕功能实现

### 下载openkylin操作系统
============
下载地址：https://www.openkylin.top/downloads/

本项目基于openKylin 2.0 SP1 X86 操作系统

### 安装
============
获取源代码
...
git clone https://gitlink.org.cn/kylin-video.git
...

安装必要的编译工具和库：
cd kylin-video
cd subtitle_generator_py
sudo apt update
python3 -m venv myenv
source myenv/bin/activate
pip install loguru
pip install torch 
pip install faster-whisper
deactivate
...

### 启动
============
...
cd ..
./run.sh
...
或者
+ 打开文件夹kylin-video/src，点击名为kylin-video的可执行文件

### 功能介绍
============
+ 原字幕功能

+ 现功能

新增或改动功能介绍如下：
#### 载入字幕
用户可选择载入原始字幕/翻译字幕
（注：当选择翻译字母时，非中文->英文 英文->中文）
![切换字幕](images\切换语言.png)
当用户选择想要的字幕语言后，点击确定，重播视频，即可实现
![中文](images\中文.png)
![英文](images\英文.png)
第一次加载字幕需要耐心等待30秒左右
#### 字体颜色
用户可选择自己喜欢的颜色，点击确定后，重播视频，即可实现

#### 字幕位置
用户可选择字幕位置底部/顶部，点击确定好，重播视频，即可实现

