
毕业的同学即将成为校友，本文的目的是指导你如何修改小组页面的“团队成员”页面(https://seu-netsi.net/team/)[https://seu-netsi.net/team/]，
把自己信息移动到“校友（Alumni）”栏目中，并添加自己的硕士论文标题，及修改其他信息。

## 数据目录与内容简介

网站的所有数据都在`_data`文件目录下面。具体包括
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/news.yml
  - 研究小组的新闻信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/research.yml
  - 研究小组的科研方向信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/publist.yml
  - 研究小组的论文发表情况。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/staff_members.yml
  - 研究小组教师信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/phd_members.yml
  - 研究小组的博士信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/master_members.yml
  - 研究小组的硕士信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/undergraduate_members.yml
  - 研究小组的本科生信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/alumni_members.yml
  - 研究小组的毕业生信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/alumni_others.yml
  - 研究小组的其他毕业生信息。
- https://github.com/SEU-NetSI/seu-netsi.github.io/blob/master/_data/pics.yml
  - 研究小组的照片展示信息。


## 操作步骤

步骤非常简单：把你的信息从一个yml移动到另一个yml中，并稍加修改。
1. 找你的信息。如果是硕士，信息在`master_members.yml`中。下面是一个例子。
```yml
- name: Yuming Gao
  chinese: 高钰铭
  id: gaoyuming
  photo: gaoyuming.jpeg
  info: M.Sc. Student, Started Sept. 2021
  email: withod@seu.edu.cn
  link: https://github.com/Withod
  education:
    - "<b>2021.09 ~ Now:</b> M.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Computer Science and Engineering</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
    - "<b>2017.09 ~ 2021.06:</b> B.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Computer Science and Engineering</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
  interest:
    - "<b>Algorithm design</b>"
    - "<b>UAV application</b>"
  correspondence:
    - "<b>Room:</b> 431, Computer Building, Jiulonghu Campus, SEU"
    - "<b>Github:</b> <a href='https://github.com/Withod' target='_blank'>https://github.com/Withod</a>"
```
把你的上面的信息剪切并删除。

然后，打开`alumni_members.yml`文件，粘贴进去。并且做一些修改，如下。
```yml
- name: Yuming Gao
  chinese: 高钰铭
  id: gaoyuming
  photo: gaoyuming.jpeg
  info: Master's degree in 2025,<br>Research developer at <a href='https://www.xxx.com/' target='_blank'>Xxxx Xxx</a> 
  email: withod@seu.edu.cn
  link: https://github.com/Withod
  education:
    - "<b>2021.09 ~ 2025.06:</b> M.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Computer Science and Engineering</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
    - "<b>2017.09 ~ 2021.06:</b> B.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Computer Science and Engineering</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
  thesis:
    - "面向智能无人机场的集群复杂任务调度"  
  interest:
    - "<b>Algorithm design</b>"
    - "<b>UAV application</b>"
  correspondence:
    - "<b>Room:</b> 431, Computer Building, Jiulonghu Campus, SEU"
    - "<b>Github:</b> <a href='https://github.com/Withod' target='_blank'>https://github.com/Withod</a>"
```

有几处要重点修改的地方
1. education中的毕业年份一定要修改。
```yml
  education:
    - "<b>2021.09 ~ 2025.06:</b> ... 
```
2. info中信息要修改，包括毕业就职单位。
```yml
  info: Master's degree in 2025,<br>Research developer at <a href='https://www.xxx.com/' target='_blank'>Xxxx Xxx</a> 
```
3. 添加thesis，毕业论文标题。
```yml
  thesis:
    - "面向智能无人机场的集群复杂任务调度"  
```
4. correspondence中，删除实验室工位信息。
```yml
  correspondence:
    - "<b>Github:</b> <a href='https://github.com/Withod' target='_blank'>https://github.com/Withod</a>"
```

## 照片或其他信息

可以更新一下照片，或者其他信息。


