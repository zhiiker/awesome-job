# Awesome NLP Short Questions

> 一个问题，一句回答，一张图片，简洁明了的呈现 NLP 世界的轮廓

   * [Awesome NLP Short Questions](#awesome-nlp-short-questions)
      * [速问速答](#速问速答)
         * [基础篇](#基础篇)
            * [什么是自然语言处理](#什么是自然语言处理)
            * [自然语言处理的主要任务有哪些](#自然语言处理的主要任务有哪些)
            * [文本分词的常见方法有哪些](#文本分词的常见方法有哪些)
            * [词语可以通过哪些数学方式表示](#词语可以通过哪些数学方式表示)
            * [词性标注的任务定义是什么](#词性标注的任务定义是什么)
            * [聊天机器人的常见类型有哪些](#聊天机器人的常见类型有哪些)
         * [工具篇](#工具篇)
            * [常见的分词工具包有哪些](#常见的分词工具包有哪些)
            * [有哪些好用的 NLP 工具包](#有哪些好用的-nlp-工具包)
            * [有哪些常用的 Linux 文本处理命令](#有哪些常用的-linux-文本处理命令)
         * [工作篇](#工作篇)
            * [萌新小白如何入门 NLP](#萌新小白如何入门-nlp)
            * [如何成为 NLP 算法工程师](#如何成为-nlp-算法工程师)
      * [版权问题](#版权问题)
      * [关于作者](#关于作者)
      * [参考文献](#参考文献)


## 速问速答

### 基础篇

#### 什么是自然语言处理

英语称谓为 Natural Language Processing，简称 NLP。**自然语言**指的是生活中人们使用的语言，如中文、英语，**处理**包含了对语言文本的分析、理解和生成等部分。

<div align="center"><img src="images/001.png" height="160"></div>


#### 自然语言处理的主要任务有哪些

自然语言处理的主要任务有：语音合成、语音识别、自动分词、词性标注、句法分析、文本生成、文本分类、信息检索、信息抽取、问答系统、机器翻译、自动摘要、文本逻辑推理、命名实体识别、语言模型等。

<div align="center"><img src="images/002.png" height="300"></div>


#### 文本分词的常见方法有哪些

- 基于词典的分词算法
    - 正向最大匹配法
    - 逆向最大匹配法
    - 双向匹配法
- 基于统计的机器学习算法
    - HMM 
    - CRF 
    - SVM
    - 深度学习


#### 词语可以通过哪些数学方式表示

数学表示，一般是指将词映射为向量表示，分为稀疏表示和分布表示。

- **稀疏表示**：常使用 one-hot 表示，将词映射为 n 维向量，n 为词的数目，例如总共有 10 个词，「我们」是第一个词，则其的 one-hot 向量表示为：`[1, 0, 0, 0, 0, 0, 0, 0, 0, 0]`；
- **分布表示**：较为稠密的词向量表述，可以将每个词表示为一个固定维度（例如 300 维）的向量，通常方法有 word2vec、fasttext、glove 等。


#### 词性标注的任务定义是什么

词性标注（part-of-speech tagging）,又称为词类标注或者简称标注，是指为分词结果中的每个单词标注一个正确的词性的程序，也即确定每个词是名词、动词、形容词或者其他词性的过程。


#### 聊天机器人的常见类型有哪些

根据应用场景，聊天机器人通常分为三种类型：问答系统，对话系统，闲聊机器人。

- 问答系统：基于用户的问题，给定特定回答，通常需要高质量的问答语料对；
- 对话系统：面向某一个任务，机器人和用户进行单轮、多轮交互，例如，订票机器人、客服机器人；
- 闲聊机器人：开放式领域聊天，主要用于私人助理、娱乐领域，例如微软小冰、苹果Siri等。

<div align="center"><img src="images/004.png" height="150"></div>


### 工具篇

#### 常见的分词工具包有哪些

- [Hanlp分词器](https://github.com/hankcs/HanLP)
- [结巴分词](https://github.com/yanyiwu/cppjieba)
- [Stanford分词器](https://nlp.stanford.edu/software/segmenter.shtml)
- [清华大学THULAC](https://github.com/thunlp/THULAC)
- [中科院计算所NLPIR](http://ictclas.nlpir.org/nlpir/)


#### 有哪些好用的 NLP 工具包

NLP 工具包一般包含了常见的文本处理功能，例如文本分词、词性标注、语法分析、文本分类等。国内外有一些有名的 NLP 工具包，如下：

- [HanLP](http://hanlp.com/) 中文文本处理工具包，性能较好，方法齐全；
- [NLTK](https://www.nltk.org/) 该工具包常用于教学，官方的学习资料可[在线阅读](http://www.nltk.org/book/)；
- [CoreNlP](https://stanfordnlp.github.io/CoreNLP/index.html) 由斯坦福大学开发；
- [SpaCy](https://spacy.io/) 具有工业级强度的Python NLP工具包；
- [Gensim](https://radimrehurek.com/gensim/) 从文档中自动提取语义主题，集成了多种文本表示方法；

#### 有哪些常用的 Linux 文本处理命令

1. more/less 分页查看文件内容：`more filename`
2. cat 展现整个文件的内容：`cat filename`
3. iconv 转换文本编码格式：`iconv -f utf-8 -t utf-16 inputfile -o outputfile`
4. sort 文本内容排序：`sort filename`
5. uniq 文本去重：`uniq filename`
6. join 文本连接：`join filename1 filename2`
7. grep 文本查找：`grep '你好' filename`
8. sed 操作文本，增删改，删除文件的，例如删除文件的第 2 行：`sed '2,2d' filename`
9. awk awk命令主要是将文件通过分隔符拆成列来处理，还能通过条件判断对不同的行进行不同的处理，甚至还可以进行数值计算。例如，输出第一列和第三列，分隔符为":"：`cat /etc/passwd | awk -F ':' '{print $1 "\t" $3}' `


### 工作篇

#### 萌新小白如何入门 NLP

**简单粗暴入门 NLP**

第一是动手实践，第二是加强基础。关于第一点，自学最难的不是知识的难度，而是个人的毅力，所以对于实践我都比较推荐找志同道合的朋友，做nlp的竞赛，两个人可以相互监督。关于第二点，基础我觉得是机器学习、nlp基础，还有最前沿的学术成果，要养成每周看论文的习惯。

**循序渐进入门 NLP**

- 了解NLP的最基本知识
- 了解早年经典的NLP模型以及论文
- 了解机器学习的基本模型
- 多看NLP其他子领域的论文
- 了解 CV和data mining领域的基本重大进展





#### 如何成为 NLP 算法工程师

基础功，机器学习知识 + 深度学习知识，注意其中和 NLP 相关的。

对于校招，学生期间，找份不错的实习、做个不错的竞赛或者发表一篇领域相关的论文，基本上秋招时期，都能找到工作。无论是实习、竞赛还是论文，核心都是，有什么项目，能够吸引面试官。

对于社招，工作经验，对算法、产品、业务的理解程度，能不能从零到一启动一个项目。


## 版权问题

未经授权，禁止转载，翻版必究。


## 关于作者

中科院硕士生，NLP爱好者，研究生期间，通过实习、竞赛收入超过五十万，他的一些文章：

- [读研，竞赛，与实习](https://mp.weixin.qq.com/s/7Uoz1L3SbXPRkCtJCYzVQg) 
- [如何科学的打开 Leetcode](https://mp.weixin.qq.com/s/VL0Buz0ya_LZ1AH32MJ82Q)
- [2020 年的算法，降温之后会更好](https://mp.weixin.qq.com/s/a0aaopoQ7oqgrDG8wLnBOg) 


<div><img src="images/gongzhonghao.png" height="150"></div>


## 参考文献

- [维基百科](https://zh.wikipedia.org/wiki/%E8%87%AA%E7%84%B6%E8%AF%AD%E8%A8%80%E5%A4%84%E7%90%86)
- [初入 NLP 领域的一些小建议](https://zhuanlan.zhihu.com/p/59184256)
