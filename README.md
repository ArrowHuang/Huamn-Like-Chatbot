# Huamn-Like-Chatbot
本项目主旨是让聊天机器人在对话过程中更像一个人类，整理一些目前最新的研究与本人自己的想法与实验  
目前从四个面向来让聊天机器人类人化：**个性化回复(Personalized Response Generation)**、**特定风格回复(Stylized Dialogue Response Generation)**、**情感可控回复(Emotional Response Generation)** 与 **共情回复(Empathetic Responding)**  
接下来将持续更新补充

## Personalized Response Generation  个性化回复  
- Dataset数据集
1. Wu et al. NAACL2021 Personalized Response Generation via Generative Split Memory Network 
([paper](https://aclanthology.org/2021.naacl-main.157.pdf) | [code](https://github.com/Willyoung2017/PER-CHAT))  
提出了**PER-CHAT**，一个开放领域个性化回复数据集。从AskReddit这个网站上面收集问题以及回复共计1.5M对话与300K的user，同时收集个性化的特征包括：user ID、user所有评论历史、user个人属性例如性别、居住地、喜好等 
  
2. Zhong et al. EMNLP2020 Towards persona-based empathetic conversational models
([paper](https://aclanthology.org/2020.emnlp-main.531.pdf) | [code](https://github.com/zhongpeixiang/PEC))  
提出了**PEC**，一个基于用户画像的共情回复数据集。从两个Reddit的子版块中获取数据 happy和offmychest，前者是分享开心的事情，后者是抒发郁闷的地方。同时对于对话中的每一个user，收集该user在post以及commit中的句子作为个人化信息
  
3. Zheng et al. arXiv2020 Personalized Dialogue Generation with Diversified Traits
([paper](https://arxiv.org/pdf/1901.09672.pdf) | [code](https://github.com/silverriver/PersonalDilaog))  
提出了**PD**，一个基于微博的中文个性化单轮回复数据集。从中文社交媒体Weibo中收集得到，总共20.83M的对话，8.47M的user。其中每一个user的个人信息包括Gender, Age, Location, Interest Tags以及Self Description

## Stylized Dialogue Response Generation   特定风格回复  
- Dataset数据集




## Emotional Response Generation  情感可控回复  
- Dataset数据集




## Empathetic Responding    共情回复
- Dataset数据集



