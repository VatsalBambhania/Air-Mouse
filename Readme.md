Air Mouse is an software alternative for hardware required for mouse.

The key concept here is to find a software based way to replace the requirement of hardware mouse needed to control the cursor in your computer.

Our project is still in it's beta stage and there can be several bugs in the software, given below is the instruction needed to build by yourself on you device, also feel free to report any bugs you encounter, i'll try to solve them. Also on mediapipe's official github https://github.com/google/mediapipe/issues you can lookout for common bugs and issues.


This repository contains the code and framework modules used to build the project.

PREREQUISITES:
1) Linux Opereating system (I build on UBUNTU 18.04LTS)
2) A g++ compiler (It already comes with ubuntu, but if you don't have one than install one)
3) OpenCV (If you don't have it installed already, I would recommend install it in /usr/local/bin).
4) Bazel (https://docs.bazel.build/versions/master/install-ubuntu.html shows how to install it on your system)

If you want to do it yourself, than follow the steps given below:
1) clone Air-Mouse

   $ git clone https://github.com/VatsalBambhania/Air-Mouse/
2) Go into cloned directory

   $ cd Air-Mouse
3) Start building project

   $ bazel build -c opt --copt -DMESA_EGL_NO_X11_HEADERS --copt -DEGL_NO_X11 \
   mediapipe/examples/desktop/hand_tracking:hand_tracking_gpu_cust
4) Once it is done build, in order to run solution 

   $ bazel-bin/mediapipe/examples/desktop/hand_tracking/hand_tracking_gpu_cust \
   --calculator_graph_config_file=mediapipe/graphs/hand_tracking/working_mouse.pbtxt



version https://git-lfs.github.com/spec/v1
oid sha256:dcd0e13330e57c8eca3730f4714bad046e0e4d5e2349282d73d4f87b8c68c6e0
size 5275
