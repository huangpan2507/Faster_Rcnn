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
