# 第一期书生·浦语大模型实战营

## 笔记

[第一课笔记](https://plateass.github.io/class1)

[第二课笔记](https://plateass.github.io/class2)

[第三课笔记](https://plateass.github.io/class3)

[第四课笔记](https://plateass.github.io/class4)

[第五课笔记](https://plateass.github.io/class5)

[第六课笔记](https://plateass.github.io/class6)

## 作业

[第二课作业](https://plateass.github.io/work2)

[第三课作业](https://plateass.github.io/work3)

[第四课作业](https://plateass.github.io/work4)

[第五课作业](https://plateass.github.io/work5)

[第六课作业](https://plateass.github.io/work6)

lmdeploy加载ptb_text_only数据集的问题
由于huggingface加载ptb_text_only数据集需要从github下载数据文件经常失败。
可以先手工现在相关文件，然后修改huggingface上的ptb_text_only.py文件，把其中三行代码修改为本地路径。
然后覆盖.cache/huggingface/modules/transformers_modules/datasets/ptb_text_only/8dxxxxxxxxx/ptb_text_only.py文件

重新执行lmdeploy。