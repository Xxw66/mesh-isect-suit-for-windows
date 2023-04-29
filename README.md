# mesh-isect-suit-for-windows
This package do some changes on mesh-insect(smplify-x), 
so that you can directly use it on windows system
to install this package with Pytorch=11.7,CUDA=11.7

Here are some problems i encountered when installed mesh-insect(smplify-x)  and how i fixed them. 
I have taken inspiration from some suggestions on the internet.
I would like to express my gratitude to those who provided the suggestions, although I will not list them individually.

1.Make sure your CUDA version and Pytorch version are compatible.

2.Chage a function in bvh.cpp, cause the function used before is no longer supported
https://blog.csdn.net/sinat_29957455/article/details/113334944

3.Move "\include/double_vec_ops.h" to "\src"
https://github.com/vchoutas/torch-mesh-isect/issues/24

4.Do some changes on "\src/bvh_cuda_op.cu"( I don't know why, but you have to, if you want install this package on windows. It works for me.)
https://gist.github.com/conorcodes/612f3358f0c2569f26e07c5fd86345fe

use this new bvh_cuda_op.cu to replaced origin file.


