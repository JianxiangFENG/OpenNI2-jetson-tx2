# OpenNI2 driver on Nvidia Jetson tx2
The original codes are cloned from OpenNI2 github page: https://github.com/occipital/OpenNI2.

By referring some online resources such as [[1]](https://www.myzhar.com/blog/the-myzharbot-project/software/configuration-nvidia-jetson-tk1/asus-xtion-pro-live-openni2-compilation-install-instructions/#Precompiled_OpenNI) and [[2]](https://www.jetsonhacks.com/2014/08/28/building-openni2-structure-sensor/), I have made further changes in `Makefile`, `CommonDefs.mak`, `CommonCppMakefile` and `Platform.Arm`. Specifically, I adapted the cpu configurations of gcc in `Platform.Arm` and added some missing macros so that the platform can be detected by the source codes.  For details please look into these files.

With the dependencies installed (I used openjdk-8-jdk mentioned by [Nvidia forum](https://forums.developer.nvidia.com/t/java-on-jetson-nano/75006/5)), after the aforementioned modifications, the source code can be compiled succesfully on a nvidia Jetson tx2 with JetPack version 4.3 (L4T 32.3.1) and Ubuntu18.04. 
