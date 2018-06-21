## 功能支持
:one: 标签识别与跟踪

:two: 物体识别与追踪

:three: 三维跟踪

## 平台支持
-----------------

Windows | Linux | MacOS |
:--------: | :------------: | :------------: |
:heavy_check_mark: | :heavy_check_mark: | :heavy_multiplication_x: |

## SDK使用
### 第一步 下载SDK
下载[最新版本SDK](https://github.com/v-iot/v-iot.github.io/releases)

### 第二步 代码示例
```
//初始化
Tag tag;
Trace trace;
trace.drawTail = false;
trace.drawCode = true;
trace.distMax = 100;
Rect frameRect(0, 0, frameWidth, frameHeight);
vector<Rect> detectRoi;
detectRoi.push_back(frameRect);
tag.Init(2, 4, 8, 16, 1, .7);

//解码
Mat frame; 
//获取图片代码逻辑
tag.Decode(frame, Rect(), 400, 15000, 0.5, 30);

//追踪
trace.Tracking(tag);

```
