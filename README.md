0.
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge
conda config --set show_channel_urls yes

conda config --show channels

# 清理缓存
conda clean --all




1.
Conda create -n 20250510qinjieyolov8 python=3.8 


2.

conda activate 20250510qinjieyolov8

3.
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

pip install torch==1.8.1+cu102 torchvision==0.9.1+cu102 torchaudio==0.8.1 -f





1.
conda env list
2.
conda activate 202505100012cbxyolov8
3.
python setup.py install


不行的话用
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple


3.
pip install -r requirements.txt

4.
Python setup.py install

pip install opencv-python

5.
运行
yolo cfg=F:\2025YOLOV8test\yolov8-main\ultralytics\yolo\cfg\default.yaml





备注：
1.
查看内存：watch -n 0.5 nvidia-smi
2.
如果是nan，就关掉所有amp
注释掉112行，batch要小

划分数据集的逻辑已经好了

(202505100012cbxyolov8) F:\2025YOLOV8test\YOLOv8-cbxmain>              pip install timm                       pip install sklearn

(202505100012cbxyolov8) F:\2025YOLOV8test\YOLOv8-cbxmain>                 pip install einops




YOLO标签的格式
object-class>        <x>          <y>       <width>      <height>
0                 0.412500     0.318981      0.358333   0.636111
               x,y是目标的中心坐标，width,height是目标的宽和高。这些坐标是通过归一化的，其中x，width是使用原图的width进行归一化；而y，height是使用原图的height进行归一化。

每个对象一行
每行的格式是：class x_center y_center width height
方框的坐标必须要归一化到（0-1），如果方框以像素为单位，请将x_center和width除以图像宽度，将y_center和height除以图像高度。
类别必须从0开始，。


