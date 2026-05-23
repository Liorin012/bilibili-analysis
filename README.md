# B站热门视频数据分析

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

# 📖 项目简介

本项目通过 B站官方 API 爬取热门视频数据，并进行多维度的数据分析与可视化。旨在探索：
1.高播放量是否等于高质量？
2.什么时间发布视频更容易获得高播放量？
3.热门视频的标题有什么共同特征？

核心发现：播放量 TOP10 与互动率 TOP10 的视频重合度仅为 30%，验证了“高播 、放 ≠ 高质量”的结论。

# 📊 数据概览

| 指标 | 数值 |
|--------|--------|
| 数据总量 | 171 条 |
| 时间范围 | 2025年5月（近期热门）|
| 数据维度 | 7 个字段 |
| 分类覆盖 | 全站 / 动画 / 音乐 / 游戏 / 知识 / 娱乐 |

# 数据字段说明．

| 字段 | 说明 |
|------|------|
| bvid | 视频唯一标识 |
| title | 视频标题 |
| view | 播放量 |
| like | 点赞数 | 
| coin | 投币数 |
| favorite | 收藏数 |
| reply | 评论数 |
| pubdate | 发布时间（时间戳）|

#🔧 技术栈

| 类别 | 技术 |
|------|------|
| 爬虫 | Python + Asyncio + bilibili-api-python |
| 数据处理 | Pandas |
| 可视化 | Matplotlib + Seaborn + WordCloud |
| 中文分词 | Jieba |
| 开发环境 | PyCharm + Virtual Environment |

# 📁 项目结构
bilibili-analysis/
├── spider.py # 爬虫代码
├── analysis.py # 数据分析代码
├── bilibili_dataset.csv # 原始数据集
├── high_freq_words.txt # 高频词统计
├── images/ # 可视化图表
│ ├── 图1_播放量分布.png
│ ├── 图2_播放量与点赞关系.png
│ ├── 图3_互动率分布.png
│ ├── 图4_评论数分布.png
│ ├── 图5_词云图.png
│ ├── 图6_小时平均播放量.png
│ ├── 图7_小时发布数量.png
│ ├── 图8_星期平均播放量.png
│ └── 图9_时间热力图.png
├── requirements.txt # 依赖库
└── README.md # 项目说明
