
每年都有新同学加入到实验室，本文的目的是指导你如何在小组页面的“团队成员”页面https://seu-netsi.net/team/
中，把自己的信息添加到“博士（PhD）”栏目或者“硕士（Master）”栏目或者“本科生（Undergraduate）”栏目中。

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

步骤非常简单：先找到存储你对应身份信息的文件，再添加你的照片。
1. 添加个人信息：在 `_data`文件夹里找到你的身份对应的文件，例如：如果你是博士，打开`phd_members.yml`并添加信息;
如果你是硕士生，打开`master_members.yml`并添加信息;如果你是本科生，打开`undergraduate_members.yml`并添加信息。
下面是一个例子。
```yml
- name: Hao Li
  chinese: 李昊
  id: lihao
  photo: lihao.jpg
  info: M.Sc. Student, Started Sept. 2024
  email: 1365101196@qq.com
  link: https://github.com/eurkaaaa
  education:
    - "<b>2024.09 ~ Now:</b> M.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Computer Science and Engineering</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
    - "<b>2020.09 ~ 2024.06:</b> B.Sc, <a href='https://cse.seu.edu.cn/main.htm' target='_blank'>School of Artificial and Intelligence</a>, <a href='https://www.seu.edu.cn/' target='_blank'>Southeast University</a>, China"
  interest:
    - "<b>Internet of Things</b>"
    - "<b>Algorithm Design</b>"
  correspondence:
    - "<b>Github:</b> <a href='https://github.com/eurkaaaa' target='_blank'>https://github.com/eurkaaaa</a>"
  thesis: placeholder  
  gradinfo: placeholder 
```
参考上面的样式信息，编写你自己的相关内容，添加到对应的yml文件当中。


2. 添加个人照片：把你的照片（如`zhangsan.jpg`）上传到 `images/teampic`文件夹里，比例裁剪成方形，大小控制在100KB以内，因为页面展示尺寸很小。

