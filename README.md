# datihelper

### Android手机百万英雄，芝士超人，冲顶大会等答题助手。自动提取题目，然后调用百度网页进行搜索。


##### 各APP对应的运行文件

- 百万英雄运行baiwan.py文件
- 芝士超人运行zhishi.py文件
- 冲顶大会运行chongding.py文件

使用方法：

1. 答题过程中，数据线连接手机，开启USB调试模式。
2. 当题目出现的瞬间，执行对应APP的脚本。
3. 从自动弹出的百度网页搜索结果寻找答案。


说明：

1. 原理使用的是adb.exe截屏Android手机屏幕，使用python的PIL图像库截取题目区域，使用百度OCR接口进行文字识别，然后调用百度搜索接口进行搜索。
2. 题目区域与手机大小有关，如果出现题目区域截取不正确，请调整`box = (0, 200, 680, 400)`中坐标位置。
3. 百度免费OCR接口有500次/天调用量限制，请合理使用。
4. 代码中将图片“**写在本地磁盘再读取出来**”这个过程实际上会浪费一点时间，影响最后搜索结果出现的速度，可以进行优化。
5. 百度API调用需要使用APP_ID、API_KEY、SECRET_KEY三个key, 请自行注册百度AI平台，按照官方说明获取。
6. 脚本运行可能与环境有关，如果无法运行，请确认环境配置正确，包安装完全，本脚本在Python2.7下运行。
7. 一切结果仅供参考和娱乐。


![](https://i.imgur.com/caG2uWf.png)

![](https://i.imgur.com/T6zNqiq.jpg)

![](https://i.imgur.com/21Em0Dq.png)

