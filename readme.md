    Created by lucy on 2020/11/02
#Rtsp库c++API封装
    封装成python可直接import的动态链接库
##操作流程

    编译　`make`
    
    运行示例`python3 rtsp.py`
    
    清除编译内容　`make clean`

## 问题＆解决
    １．报错 mpp_log: decode_get_frame failed, return -8.
    
    解决：先验证摄像头是否能拉去到视频流，如果在你的PC上可以，但是代码依然报错，
    那么在板子上用cv2.VideoCapture尝试能否拉到视频流，如果报错method DESCRIBE failed: 401 Unauthorized
    就重启摄像头即可