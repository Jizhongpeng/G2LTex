# G2LTex

This repesitory contains G2LTex, a implementation of global-to-local texture optimization for 3D Reconstruction with RGB-D Sensor based on [mvs-texturing](https://github.com/nmoehrle/mvs-texturing). More information and the paper can be found [here](http://graphvision.whu.edu.cn/).

# How to use

## 1. run
To test our algorithm. run G2LTex in command lien:
```
./bin/G2LTex [DIR] [PLY] 
```
Params explanation:
-`PLY`: The Reconstrucion model for texture mapping.
-`DIR`: The texture image directory, include rgb images, depth images, and camera trajectory.

The parameters of the camera and the system can be set in the configure file.
```
Config/config.yml
```

How install and run this code.
```
git clone https://github.com/fdp0525/G2LTex.git
cd G2LTex/bin
./G2LTex ../Data/bloster/textureimages ../Data/bloster/bloster.ply
```
## 2. Input Format
- Color frames (color_XX.jpg): RGB, 24-bit, JPG.
- Depth frames (depth-XX.png): depth (mm), 16-bit, PNG (invalid depth is set to 0).
- Camera poses (color_XX.cam): world-to-camera [tx, ty, tz, R00, R01, R02, R10, R11, R12, R20, R21, R22].


## 3. Dependencies
The code and the build system have the following prerequisites:
- ubuntu 16.04
- gcc (5.4.0)
- OpenCV (2.4.10)
- Eigen(>3.0)
- png12
- jpeg

# Publication
If you find this deome valuable for your reseach, please cite our works.

> Y. Fu, Q. Yan, L. Yang, J. Liao and X. Chun. Texture Mapping for 3D Reconstruction with RGB-D Sensor. In CVPR. 2018.



