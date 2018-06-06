BootStrap: docker
From: nvidia/cuda:8.0-cudnn6-runtime-ubuntu16.04

################################################################################
%labels
################################################################################
MAINTAINER Ovcharenko Group

################################################################################
%environment
################################################################################
export PATH=/usr/local/sbin:/usr/sbin:/sbin:/bin:/usr/bin:/usr/local/bin:/usr/local/cuda/bin:
export PYTHONPATH=/usr/share/pdb2pqr:

################################################################################
%post
################################################################################

###
### install keras + tensorflow + other useful packages
###
apt-get update
apt-get install -y graphviz locales python python-pip git python-vtk pdb2pqr python-pandas
locale-gen en_US.UTF-8
apt-get clean

pip install --upgrade pip
pip install tensorflow-gpu==1.4.0
pip install keras==2.0.8
pip install setuptools wheel Pillow scikit-learn matplotlib ipython==5.5.0
pip install --upgrade notebook
pip install cython
pip install Biopython
pip install Tensorboard

###
### destination for NIH HPC bind mounts
###
mkdir /gpfs /spin1 /gs2 /gs3 /gs4 /gs5 /gs6 /gs7 /gs8 /data /scratch /fdb /lscratch /pdb
