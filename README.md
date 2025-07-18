# 视频字幕AI自动识别显示工具

>  本项目是在开源项目[openkylin-video](https://github.com/openkylin/kylin-video) 基础上进行视频字幕功能实现

> [!NOTE]
> 鉴于赛题要求，本项目仅实现了字幕识别及显示等相关功能，因此对于开源项目kylin-video播放器原有的其他功能进行了保留，但未对其他功能（例如“设置”中的“播放设置”、“音频设置”等）测试，所以不能保证它们能够正常响应。
>
> 如果误触到字幕以外的功能，产生异常，重新启动播放器播放视频即可。
> 
> 建议严格按照README启动，并参考“实验测试”章节测试本项目的字幕相关功能。

## openKylin 2.0 SP1 X86 操作系统实现该项目

- 下载地址：[官网](https://www.openkylin.top/downloads/)


### 安装

- 获取源代码

```cmd
git clone https://gitlink.org.cn/kylin-video.git
```

- 安装虚拟python环境和依赖库
  
```cmd
cd kylin-video
cd subtitle_generator_py
sudo apt update
python3 -m venv myenv
source myenv/bin/activate
pip install loguru torch translate faster-whisper numpy ffmpeg-python -i https://pypi.tuna.tsinghua.edu.cn/simple
deactivate
```

### 启动

- 方式一
  
```cmd
cd ..
./run.sh
```
如果显示权限不够，则执行

```cmd
chmod +x run.sh src/kylin-video
```
- 方式二
  
直接点击run.sh

- 方式三
  
打开文件夹kylin-video/src，点击名为kylin-video的可执行文件

### 视频播放

本项目是在[openkylin-video](https://github.com/openkylin/kylin-video) 上进行视频字幕功能实现，由于openkylin系统自带kylin-video播放器，为避免系统默认播放器自动接管视频播放，需在完成上述程序启动操作后，通过拖放视频文件至应用窗口执行播放。

### 功能介绍
本项目在开源代码[openkylin-video](https://github.com/openkylin/kylin-video) 的基础上，新增了字幕语言切换、字幕颜色自定义、字幕位置设置功能。

具体功能实现及操作，见项目说明书第三章。
