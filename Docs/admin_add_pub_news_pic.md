## 添加刊物
在Publication页面添加刊物条目
### 操作步骤
在data/publist.yml文件中复制之前的一条刊物条目代码，粘贴后修改，以下面这个条目的代码为例：
- id：作者姓氏首字母-期刊缩写+年份
- category: 有uwbswarmrl、uavpathplan、harvestingnet、adhocnetworkingrs、uavedgecomputing几个分类，在条目中添加分类标签后，刊物条目也会在Research页面相应的研究方向中展示
- 其余信息可仿照其他条目来填写

```yml
- id: LSLCWC-RAL25
  year: 2025
  authors: Shushuai Li, Feng Shan, Jiangpeng Liu, Mario Coppola, Christophe De Wagter, and Guido de Croon
  title: "Onboard Ranging-based Relative Localization and Stability for Lightweight Aerial Swarms"
  pubinfo: "IEEE Robotics and Automation Letters (<b>RA-L</b>) , Conditionally Accepted on Jun 15, 2025."
  link:
    paper: https://shushuai3.github.io/autonomous-swarm/
    code: https://github.com/shushuai3/cf_onboard_swarm/tree/swarm
    slide: placeholder
    video: https://www.youtube.com/playlist?list=PL_KSX9GOn2P9sgaX3DHnPsnBCJ76fLNJ5
    doi: placeholder
  highlight: 
    attr: 0
  bibtex: placeholder
  category: uwbswarmrl
```

## 添加新闻
在网站首页右侧新闻栏添加新闻条目
### 操作步骤
在data/news.yml文件中复制之前的一条新闻条目代码，粘贴后修改，以下面这个条目的代码为例：
```yml
- date: June 15, 2025
  headline: "Our paper `<a href='https://shushuai3.github.io/autonomous-swarm/'>Onboard Ranging-based Relative Localization and Stability for Lightweight Aerial Swarms</a>' was conditionally accepted by IEEE Robotics and Automation Letters (RA-L)."

```

## 添加画廊图片
在Gallery页面添加图片
### 操作步骤
在data/pics.yml文件中 ourgroup 复制之前的一条图片条目代码，粘贴后修改，以下面这个条目的代码为例：
- id：日期+活动名
- image：
  - 命名：日期 + 活动
  - 尺寸：2048 * 1152 像素
- intro：会展示在图片下方的图片介绍

```yml
- id: 2024_11_02_Autumn_Outing
  image: 2025_06_06_Graduation.jpg
  intro: "Graduation Memory 2025"
  date: "2025-06-06"
```
