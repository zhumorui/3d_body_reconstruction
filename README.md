# 3d_body_reconstruction
### This project is a detailed step description of octopus. Find this project from https://github.com/thmoa/octopus
通过多张图像对人体图像进行3维重构。 简单来说就是利用ffmpeg对视频进行拆帧处理（我采用的方法是获取人体每旋转45度获得的图片，一共为八张），[OpenPose——Body25_face](https://github.com/CMU-Perceptual-Computing-Lab/openpose)对人体关键点和脸部进行检测，获得具有关键点信息和人脸的json文件，利用[CIHP_PGN](https://github.com/Engineering-Course/CIHP_PGN)人体图像分割图片，可以对人体不同身体部位进行分割。最后再利用ocotopus项目恢复人体的3维结构。3d重构具体原理详见https://github.com/thmoa/octopus，本项目只介绍详细步骤，和提供自己所写的一些python脚本用于对图像进行的前期预处理。
## 环境
本项目采用Ubuntu20.04系统，按理说应该支持ubuntu16.04及以上版本。深度学习环境：为了避免环境冲突，我用anaconda建立了两个虚拟环境，一个为[octopus](https://github.com/thmoa/octopus)，一个为[CHIP_PGN](https://github.com/Engineering-Course/CIHP_PGN)
## Installation
~~~
git clone https://github.com/zhumorui/3d_body_reconstruction.git
~~~
