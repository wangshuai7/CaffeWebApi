- 使用指导
 - 阅读环境配置http://blog.csdn.net/qq_24328101/article/details/72837466，安装完caffe环境后，保持本目录文件结构进行使用（如需修改目录结构，请阅读flask关于文件配置的位置的文档，以及修改源码中关于model和图片的路径）
 - ```cd server ``` then ``` python server.py```，默认使用5000端口并且打开了外网访问（host='0.0.0.0'）和debug模式(debug=True)，在不需要的时候可以在server.py 的app run里修改
 - algrithm.py 提供两种api，一种是转换成json前的字典，另一种是json，按参数分类，分别提供输入图片(cv2打开的数据格式)和输入图片路径两种，实际上都是在调用前者
 - http://IP:5000/all , http://IP:5000/cascade, http://IP:5000/gender, http://IP:5000/age,4个web demo页面
 - http://IP:5000/api/v1.0/all,http://IP:5000/api/v1.0/cascade,http://IP:5000/api/v1.0/gender,http://IP:5000/api/v1.0/age ,4个api，post图片文件，返回json结果
