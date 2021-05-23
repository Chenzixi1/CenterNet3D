# CenterNet3D
CenterNet3D

### Data preparation

Download and unzip the full KITTI detection dataset to the folder /path/to/kitti/. Then place a softlink (or the actual data) in data/kitti/. There are two widely used training/validation set splits for the KITTI dataset. Here we only show the setting of split1, you can set split2 accordingly.

cd D4LCN
ln -s /path/to/kitti data/kitti
ln -s /path/to/kitti/testing data/kitti_split1/testing

python data/kitti_split1/setup_split.py
python data/kitti_split1/setup_depth.py

sh data/kitti_split1/devkit/cpp/build.sh

cd lib/nms
make
