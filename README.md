# Tensorflow- Human- Pose- Estimation- Using- OpenPose

# NOTE: This Readme file is only applicable for installing all the repositories correctly into a single place and then satisfying all the dependencies. Code can also be used onto Google Colaboratory

'Openpose', human pose estimation algorithm, have been implemented using Tensorflow. It also provides several variants that have some changes to the network structure for **real-time processing on the CPU or low-power embedded devices.**

**You can even run this on your macbook with a descent FPS!**

Original Repo(Caffe) : https://github.com/CMU-Perceptual-Computing-Lab/openpose

### Dependencies

You need dependencies below.

- python3
- tensorflow 1.4.1+
Just refer to the requirements file I have posted in the repository and install all the libraries using pip command.
```bash
$ pip3 install -r requirements.txt
```

### Install

Clone the repo and install 3rd-party libraries.

```bash
$ git clone https://www.github.com/theRishabhJainRJ/Human-Pose-Estimation-Part-1
$ git clone https://www.github.com/theRishabhJainRJ/Human-Pose-Estimation-Part-2
```

Make sure all the files and folders are present in the same parent folder.

Build c++ library for post processing. See : https://github.com/theRishabhJainRJ/Human-Pose-Estimation-Part-2/tree/master/tf_pose/pafprocess

```
$ cd tf_pose/pafprocess
$ swig -python -c++ pafprocess.i && python3 setup.py build_ext --inplace
```


### Download Tensorflow Graph File(pb file)

CMU's model graphs are too large for git, so I uploaded them on an external cloud. You should download them if you want to use cmu's original model. Download scripts are provided in the model folder.

```
$ cd models/graph/cmu
$ bash download.sh
```
