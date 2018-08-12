# 训练基于句法规则的特殊词向量

### 简介
代码源自word2vec的原作者，代码请见：

* [Word2vec](https://code.google.com/archive/p/word2vec/)

可用大规模训练语料可使用维基等的公开articles: 
* http://mattmahoney.net/dc/enwik9.zip 
* http://dumps.wikimedia.org/enwiki/latest/enwiki-latest-pages-articles.xml.bz2

### 使用设置
* 数据处理： 依存关系可使用句法依存或语义依存（需外部包支持，如斯坦福core-nlp或ltp-nlp）。
* 维基数据预处理及切分可使用相关工具（包含在工程中）。
  
### 开始训练
* 执行脚本即可，其中参数可根据需求及硬件环境自行设置。
 
### 注意
* 过多的线程（>200）可能会导致segment fault，并会导致训练效果下降；
* 依存关系的阶数会影响训练效果，5-7阶便基本稳定；
* 虽然我们在训练依存关系时采用了亚采样，但其频率相差悬殊，应选取相对平衡的语料来进行训练。
