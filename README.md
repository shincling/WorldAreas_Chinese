# WorldAreas_Chinese
Raw chinese text for the main areas in across the world-wide area. 世界主要地区的中文地名纯文本

## Info:
原始数据及提供来自于： https://github.com/chency148/worldArea

这里根据world-areas进行了简单的格式化和抽取，直接提供最原始的纯文本文件（以.py列表存储）.

纯文本文件可以在大概5个vim命令内处理完成。

## Motivations:
Project中需要对交互中的地名进行简单的定位。

初步尝试直接用Jieba的词性标注来找到地点（ns标识）解决，可能存在很多主要地名无法识别到的情况，如：
"18日傍晚，在菲律宾首都马尼拉著名的罗哈斯大道。"的词性标注结果是：

```
18 m
日 m
傍晚 t
， x
在 p
菲律宾 ns
首都 d
马尼拉 nr
著名 a
的 uj
罗哈斯 nr
大道 n
。 x
```
其中“马尼拉”没有被正确标识，被标识为了nr（人名）。

故整理一下中文地名，额外进行一次匹配。

PS：也可以直接添加到Jieba的分词词典当中。


## Thanks:
感谢原作chency148的原始数据来源。
