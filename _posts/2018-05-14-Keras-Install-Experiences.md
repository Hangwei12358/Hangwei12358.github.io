---
layout: post
title: "Keras Install Experiences"
date: 2018-05-14
---

May.14.2018 
Successfully install TensorFlow, Keras in lily server. 

### Main idea
The main idea is to follow the instructions on official websites! For instance, when installing cuda related applications, it's better to follow the instructions on cuda websites instead of those on TensorFlow websites.

### Install cuda
One very important experience:
when install cuda, follow the instructions on its official website instead of those on tensorflow website, etc. 
### pip problem
>  from pip._internal import main ImportError: No module named 'pip._internal'

if there is some error when using pip or pip3, the reason is there might be many versions of pips in different applications/exes. The solution is to uninstall pip and reinstall pip.


### Install cudnn
there is one mistake after installation. 
The error is 
>/usr/local/cuda/include/cuda_runtime_api.h:1683:101: error:  use of enum  ‘cudaDeviceP2PAttr’ without previous declaration

The solution is: to change the file /usr/include/cudnn.h,  I changed the line:
```
#include "driver_types.h" 
```
to
```
#include <driver_types.h>
```

Test the Keras with examples in official
```
curl -sSL https://github.com/fchollet/keras/raw/master/examples/mnist_mlp.py | python
```
without GPU in lily server: ~2min

with GPU in lily server: ~1min


