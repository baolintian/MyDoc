## 视音频处理入门

记录一些必备的知识点。

首先入门教程：[[总结]FFMPEG视音频编解码零基础学习方法](<https://blog.csdn.net/leixiaohua1020/article/details/15811977>)

可以发现这个作者的文笔非常的清晰，注释非常的清楚，值得学习。

该作者[雷霄骅](https://blog.csdn.net/leixiaohua1020)为中国传媒大学博士生，不幸因劳累过度逝世，缅怀作者。



### 基本思路

本质上是一种__评价视频精彩程度__，来进行相应的剪辑合成。

#### 基本单元

1. 根据弹幕信息获取key segment，获得起始时间和持续时间。
2. 下载弹幕`.xml`，并且只获得改时间片段内的，生成`.ass`字幕转带有透明层的`.mov`
3. 下载视频，截取该片段
4. 合并`.mov`与`.mp4`

#### 连接单元

1. 过渡动画，bgm
2. 加入标题和名字，持续时间为3s



#### 爬取单元

1. 固定时间间隔获取相关的视频列表，进行数据库的存储，此刻的弹幕信息可能还不足，不需要进行分析，只需要记住名字就行了，以及下载相应的视频。