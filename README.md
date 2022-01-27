# Huamn-Like-Chatbot
本项目主旨是让聊天机器人在对话过程中更像一个人类，整理一些目前最新的研究与本人自己的想法与实验  
目前从四个面向来让聊天机器人类人化：**个性化回复(Personalized Response Generation)**、**特定风格回复(Stylized Dialogue Response Generation)**、**情感可控回复(Emotional Response Generation)** 与 **共情回复(Empathetic Responding)**  
接下来将持续更新补充

## Personalized Response Generation  个性化回复  
- Dataset数据集
1. Wu et al. NAACL2021 Personalized Response Generation via Generative Split Memory Network 
([paper](https://aclanthology.org/2021.naacl-main.157.pdf) | [code](https://github.com/Willyoung2017/PER-CHAT))  
提出了***PER-CHAT***，一个开放领域个性化回复数据集。从AskReddit这个网站上面收集问题以及回复共计1.5M对话与300K的user，同时收集个性化的特征包括：user ID、user所有评论历史、user个人属性例如性别、居住地、喜好等 
  
2. Zhong et al. EMNLP2020 Towards persona-based empathetic conversational models
([paper](https://aclanthology.org/2020.emnlp-main.531.pdf) | [code](https://github.com/zhongpeixiang/PEC))  
提出了***PEC***，一个基于用户画像的共情回复数据集。从两个Reddit的子版块中获取数据 happy和offmychest，前者是分享开心的事情，后者是抒发郁闷的地方。同时对于对话中的每一个user，收集该user在post以及commit中的句子作为个人化信息
  
3. Zheng et al. arXiv2020 Personalized Dialogue Generation with Diversified Traits
([paper](https://arxiv.org/pdf/1901.09672.pdf) | [code](https://github.com/silverriver/PersonalDilaog))  
提出了***PD***，一个基于微博的中文个性化单轮回复数据集。从中文社交媒体Weibo中收集得到，总共20.83M的对话，8.47M的user。其中每一个user的个人信息包括Gender, Age, Location, Interest Tags以及Self Description

4. Zhang et al. ACL2018 Personalizing Dialogue Agents: I have a dog, do you have pets too?
([paper](https://arxiv.org/pdf/1801.07243.pdf) | [code](https://github.com/facebookresearch/ParlAI))   
提出了***PERSONA-CHAT***(***PC***)，包含了1K多个性格，标记人员需要按照给定的性格来建构对话，这个数据集是全靠annotator根据给定的性格写对话，其他相关的研究都是采用社交媒体上现有的数据以及用户个人信息介绍来构建

5. Mazare et al. ENMLP2018 Training Millions of Personalized Dialogue Agents
([paper](https://arxiv.org/pdf/1809.01984.pdf) | [code](https://github.com/Exe-dev/PersonaGeneration))  
提出了***PCR***，第一个基于Reddit的个性化信息数据集。首次提出从Reddit中获取user的post以及commit作为个人信息，共收集700M的基于个性化的对话以及5M人信息

## Stylized Dialogue Response Generation   特定风格回复  
- Dataset数据集
1. Zheng et al. AAAI2021 Stylized Dialogue Response Generation Using Stylized Unpaired Texts
([paper](https://arxiv.org/pdf/2009.12719.pdf) | [code](https://github.com/silverriver/Stylized_Dialog))  
提出了***WDJN***金庸风格回复生成数据集。收集了300K的微博数据(Style S0)，然后从金庸小说中采样95.1K人物说话unpaired句子(Style S1)

2. Li et al. NeurIPS2021 Stylized Dialogue Generation with Multi-Pass Dual Learning
([paper](https://proceedings.neurips.cc/paper/2021/file/ef67f7c2d86352c2c42e19d20f881f53-Paper.pdf) | [code](https://github.com/codebaseli/mpdl))  
提出了***SDGC***莎士比亚风格回复生成数据集。从Twitter、Yahoo上面搜集对话回复，然后利用莎士比亚剧本训练风格

3. Gao et al. EMNLP 2019 Structuring Latent Spaces for Stylized Response Generation
([paper](https://aclanthology.org/D19-1190.pdf) | [code](https://github.com/golsun/StyleFusion))  
提出了***STYLEFUSION***一个具有arXiv以及Holmes风格回复生成数据集。从arXiv这个网站收集1998到2002的文章共100万个句子，并从福尔摩斯系列小说中提取38K个句子

4. Niu and Bansal TACL Journal 2018 Polite Dialogue Generation Without Parallel Data
([paper](https://aclanthology.org/D19-1190.pdf) | [code](https://github.com/golsun/StyleFusion))  
提出了***Stanford Politeness Corpus***斯坦福礼貌风格回复数据集。从开放式问答网页（包含Wikipedia editor's talk page以及Stack Exchange QA communities）中收集，并标注了粗鲁及礼貌的回复

## Emotional Response Generation  情感可控回复  
- Dataset数据集
1. Zhou et al. AAAI2018 Emotional Chatting Machine: Emotional Conversation Generation with Internal and External Memory  
([paper](https://arxiv.org/pdf/1704.01074.pdf) | [code](https://github.com/tuxchow/ecm))  
提出了***ESTC***(***Emotional STC***)数据集，先是在NLPCC数据集上训练情感分类器，然后在STC数据集上自动打上7类情感标签(Angry, Disgust, Happy, Like, Sad, Other)，总共包含217,905段对话  

2. Lubis et al. AAAI2018 Eliciting Positive Emotion through Affect-Sensitive Dialogue Response Generation: A Neural Network Approach
([paper](https://ahcweb01.naist.jp/papers/conference/2018/201802_AAAI_nurul-lu_1/201802_AAAI_nurul-lu_1.paper.pdf) | code)  
在SubTle对话数据集上，使用SEMAINE情感分类数据(包含了8类的情感Alert, Excited, Elated, Happy, Content, Serene, Relaxed, Calm)去标注数据，最后得到2,349笔对话  

3. Huang et al. NLPCC2017 Overview of the NLPCC 2017 Shared Task: Emotion Generation Challenge
([paper](http://coai.cs.tsinghua.edu.cn/hml/media/files/Overview_of_the_NLPCC_2017_Shared_Task__Emotion_Generation_Challenge.pdf) | [Link](http://tcci.ccf.org.cn/conference/2017/dldoc/taskgline04.pdf))  
清华黄民烈教授在NLPCC上发布了一个情感可控回复生成的数据集，该数据集是从微博的发文及回复中抽取，共计5000段。每段发文与回复都有一个情感的标签，一共分成五种情感(Like, Sad, Disgust, Angry, Happy)

## Empathetic Responding    共情回复
- Dataset数据集
1. Welivita et al. EMNLP2021 A Large-Scale Dataset for Empathetic Response Generation
([paper](https://aclanthology.org/2021.emnlp-main.96.pdf) | [code](https://github.com/anuradha1992/EDOS))  
提出了EDOS，一个基于电影字幕的大规模的共情回复数据集。从OpenSubtitles电影字幕语料库中搜集4M的数据，并且用一个分类器（在 EmpatheticDialogues 数据集上 训练的BERT分类器）给数据打上标签最终得到1M的带有情绪标签的对话。该数据集包含了32中的情绪、8种共情回复的意图（Questioning; Agreeing; Acknowledging; Sympathizing; Encouraging; Consoling: Suggesting; and Wishing）还有中性的标签

2. Zhong et al. EMNLP2020 Towards persona-based empathetic conversational models
([paper](https://aclanthology.org/2020.emnlp-main.531.pdf) | [code](https://github.com/zhongpeixiang/PEC))  
提出了***PEC***，一个基于用户画像的共情回复数据集。从两个Reddit的子版块中获取数据 happy和offmychest，前者是分享开心的事情，后者是抒发郁闷的地方。同时对于对话中的每一个user，收集该user在post以及commit中的句子作为个人化信息

3. Rashkin et al. ACL2019  Towards Empathetic Open-domain Conversation Models: a New Benchmark and Dataset
([paper](https://arxiv.org/pdf/1811.00207.pdf) | [code](https://github.com/facebookresearch/EmpatheticDialogues))  
提出了EMPATHETICDIALOGUES，一个共情回复生成的Benchmark数据集。数据集包括24,850 个关于不同情绪的情景下的对话，收集自 810 位不同的参与者，其中关于情绪的标签一共
有32种
