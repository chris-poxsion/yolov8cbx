"""
Module: personal_info
Author: Boxin Cao
Email: cbx2018cn@foxmail.com
Website: https://caobo.xin
Version: 3.1.9
Python Version: >= 3.8
License: MIT License 

Copyright (c) 2023  By CaoBoxin
All rights reserved.

"""
**无废话 三步极速安装 自研爆改包-yolov8cbx**

1.
Conda create -n 20250510qinjieyolov8 python=3.8
conda activate 20250510qinjieyolov8

2.
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
conda config --set show_channel_urls yes
conda config --show channels

3.
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118


*************************************************************************************
****进入编辑器****

1.
conda env list
conda activate 202505100012cbxyolov8

2.
pip install -r requirements.txt
pip install timm 
pip install einops
pip install scikit-learn
python setup.py install
pip install opencv-python
                                  ！！！！！！！！！！！
                               pip install efficientnet_pytorch
                                  ？？？？？？？？？？？？

  
3.运行
yolo cfg=F:\2025YOLOV8test\yolov8-main\ultralytics\yolo\cfg\default.yaml





备注：

查看内存：watch -n 0.5 nvidia-smi

如果是nan，就关掉所有amp
注释掉112行，batch要小

划分数据集的逻辑已经好了

conda清理环境
# 清理缓存
conda clean --all


安装不行的话用
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple


F:\2025YOLOV8test\yolov8cbx-main\cbxyolov8\ultralytics\engine
第113行             # self.args.half = self.device.type != 'cpu'  # force FP16 val during training
******改dataset train里的路径！******


YOLO标签的格式
object-class>        <x>          <y>       <width>      <height>
0                 0.412500     0.318981      0.358333   0.636111
               x,y是目标的中心坐标，width,height是目标的宽和高。这些坐标是通过归一化的，其中x，width是使用原图的width进行归一化；而y，height是使用原图的height进行归一化。

每个对象一行
每行的格式是：class x_center y_center width height
方框的坐标必须要归一化到（0-1），如果方框以像素为单位，请将x_center和width除以图像宽度，将y_center和height除以图像高度。
类别必须从0开始，。


F:\2025YOLOV8test\yolov8-main\ultralytics\yolo\cfg\default.yaml


Ultralytics YOLOv8.0.202  Python-3.8.20 torch-2.4.1+cu118 CUDA:0 (NVIDIA GeForce GTX 1650, 4096MiB)
"""
Module: personal_info
Author: Boxin Cao
Email: cbx2018cn@foxmail.com
Website: https://caobo.xin
Version: 3.1.9
Python Version: >= 3.8
License: MIT License 

Copyright (c) 2023  By CaoBoxin
All rights reserved.

"""
