# gradio内网加载慢的问题

版本4.29
目录位置/path to conda/anaconda3/envs/conda name/lib/python3.xx/site-packages/gradio

1. 修改 themes/utils/fonts.py
   搜索googleapis
   修改为 return ''#f'.......
2. 修改templates/frontend/index.html
   搜索cdnjs
   修改为src="assets/iframeResizer.contentWindow.min.js"//"http://cdnjs.......
3. 代码中添加os.environ['GRADIO_ANALYTICS_ENABLED']='False'

版本3.36.1
之前搜到过一个网页，照着改就行了现在找不到了。

# Chromadb 禁止访问posthog

代码中增加，[参考](https://github.com/zylon-ai/private-gpt/issues/34#issuecomment-1543930590)
例如在langchain中调用
from chromadb.config import Settings
db = Chroma(...,client+settings=Settings(anonymized_telemetry=False))
这是chromadb中
db = Chroma.from_documents(texts, llama, persist_directory=persist_directory, client_settings={"anonymized_telemetry": False})

# Tensorflow不能加载TensorRT的问题

tensorflow 2.16之后删除了tensorflow-gpu(最后版本停留在2.11版)。
tensorflow 2.16 [安装要求](https://tensorflow.google.cn/install/gpu?hl=zh-cn):gpu驱动450以上版本,cuda 11.2,tensorRT 6.0, cudnn 8.1
pytorch已经开始用cuda 12了,所有好麻烦的。

在tensorflow 2.11.0下，安装了tensorflow-gpu 2.11之后总算支持tensorRT了。
但是tensorflow 2.16.1没搞定tensorRT，好像连cudnn都没有加载成功。训练推理速度是上面的3倍。
