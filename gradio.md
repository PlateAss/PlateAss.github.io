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