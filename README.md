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
git clone https://gitlink.org.cn/xU6YmmUDv2/spzmazdsbxsgj.git
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

该播放器不支持循环播放、自动播放下一个视频，每次播放完视频，需手动点击下一个要播放的视频。

### 功能介绍
本项目在开源代码[openkylin-video](https://github.com/openkylin/kylin-video) 的基础上，新增了字幕语言切换、字幕颜色自定义、字幕位置设置功能。

此处只做简单介绍，具体功能实现及操作，见项目说明书第三章。
- 字幕语言切换
    - 右上角三横-设置-字幕设置-字幕语言切换（原始语言/翻译）
    - 提供“原始语言”和“翻译”两种字幕加载选项，用户只能二选一，避免字幕混乱。（注：当选择“翻译”模式时，如果原始语言是非英文，则会自动翻译为英文；如果原始语言为英文，则会翻译成中文。
    - 当用户选择想要的字幕语言后，点击确定，需要手动重播视频，即可实现（注：如果是打开未生成过字幕的视频，因调用模型识别，需要黑屏等待30s左右，黑屏并非出错，请耐心等待）

- 字幕颜色
    - 提供“选择颜色”按钮，点击后弹出标准颜色选择框。用户可任意选择颜色，支持全色域自定义。
    - 用户可选择自己喜欢的颜色，点击确定后，需手动点击视频进行重播，即可实现。

- 字幕位置
    - 提供下拉框，用户可根据自身偏好，选择“顶部”或“底部”显示字幕。
    - 用户可选择字幕位置底部/顶部，点击确定，重播视频，即可实现。

