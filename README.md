# ZNLP
Chinese NLP package

ZLP 是一个完全基于神经网络的自然语言处理工具包，框架采用谷歌的tensorflow，内容涵盖中文分词/ 词性标注 / 
命名实体识别 / 依存句法分析 / 关键词提取 / 文本摘要 / 文本分类 / 知识图谱 等各个领域。

## 内容列表
-安装<br>
-模块<br>
-使用<br>
-其他<br>

## 安装
初始版本并未采用任何安装方式，直接从github上clone下即可。即
git clone https://github.com/Pelhans/ZNLP
### 依赖
-tensorflow>= 1.3(更低版本的没试过，不过高于1.0的应该就可以)<br>
-pandas<br>
-numpy<br>
-tqdm<br>
sklearn<br>
scipy<br>
networkx(textrank需要)<br>
jieba(textrank可选)<br>
以上几项均通过pip 安装或运行./requirement.sh，目前仅支持python2<br>

## 模块
计划包含以下模块，其中CWS/POS/NER有时间会升级到CNN+BLSTM+CRF模型：<br>
--中文分词: 基于BLSTM神经网络，采用微软bakekoff分词语料。<br>
--词性标注： 基于BLSTM神经网络，采用人民日报1998年上半年词性标注语料库。<br>
--命名实体识别： 基于BLSTM神经网络，采用由1998年人民日报词性标注语料库处理得到的命名实体识别语料库。<br>
--依存句法分析：采用Danqi 和Mannning 2014年论文提出的神经网络结构，语料库采用清华大学语义依存分析语料库。<br>
--关键词提取：基于TextRank算法，分词&词性标注采用库内模块，也可使用结巴分词。。。<br>
--文本摘要：同样基于TextRank算法，与关键词提取处于同一模块。<br>
--文本分类：未完成<br>
--知识图谱：未完成<br>
--网络表示学习:未完成<br>

## 使用
训练与测试模型见各个文件夹中的README.md，调用模型参考pipeline文件。

## 其他
改关键词提取的过程中深刻感受到分词等基础对高层任务的影响，改进算法，任重道远啊<br>
如有问题，可以发邮件联系我:p.zhang1992@gmail.com
