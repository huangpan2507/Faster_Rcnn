# Faster_Rcnn
找到该博客：可能不支持pytorch 1.0版本
https://github.com/longcw/faster_rcnn_pytorch

Installation and demo

 1.Install the requirements (you can use pip or Anaconda):

    conda install pip pyyaml sympy h5py cython numpy scipy
    conda install -c menpo opencv3
    pip install easydict

 2.Clone the Faster R-CNN repository

    git clone git@github.com:longcw/faster_rcnn_pytorch.git

 3.Build the Cython modules for nms and the roi_pooling layer

    cd faster_rcnn_pytorch/faster_rcnn
    ./make.sh

 4.Download the trained model VGGnet_fast_rcnn_iter_70000.h5 and set the model path in demo.py

 5.Run demo python demo.py
 
 
 在进行到底3步时， 直接 ./make.sh报错File "build.py", line 2, in <module>
    import torch
ModuleNotFoundError: No module named 'torch'    然后我  sudo chmod +x ./make.sh  sudo  sh ./make.sh
 接着报错， 看一下，报错里面用的还是 python 2.版本，  然后修改  setup.py文件，  讲里面所有的 python XXX 中的python改成  python3 xxx
 然后运行， 接着报错  File "/usr/lib/python3.6/distutils/cmd.py", line 57, in __init__
    raise TypeError("dist must be a Distribution instance")
TypeError: dist must be a Distribution instance 
