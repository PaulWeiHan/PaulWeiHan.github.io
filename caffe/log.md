-----------------------------------------------------------------------------------------

**Please log all your changes on this server. Including some inportant commands history, or any software you installed. If needed, Please share the username and the password.**

Thanks.

username:renwh
password:renwh


imagenet账号：
    用户名：paulsysu
    密码：paulsysu
    
* ~/software_package: save some software package you installed
* ~/gaze : save anything about our project.
* ~/gaze/share: things about project, share with everyone
* ~/gaze/your_name: your own things

* 按下Ctrl + space，切换中文输入法。

**建议以后编译用最新的源码，编译的时候，请复制一份源码到自己的目录，在复制的的源码目录编译，不要对原始源码目录做修改。从github上下载了最新版的caffe源码，放在了 ~/gaze/share/caffe-master.zip**

to be continued

--------------------------------------------------------------------------------------------

# 2015-12-17 by Paul W. REN

1. installed chrome and "super VPN extension"(**done**)

    vpn name:       237006443@qq.com
    vpn password:   paulweihan

2. installed Teamviewer(**done**)

    ID:         708676496
    Password:   123456
3. software update (**done**)

4. bash commands

```sh
sudo apt-get install build-essential(**done**)

```

5. **copy the caffe-master code from chenl's server to ~/gaze/share/caffe-master.tar.gz** (**done**)

6. **copy the cuda-repo-ubuntu1404-7-0-local_7.0-28_amd64.deb file from chenl's server** (**done**)

    saved to ~/gaze/share/cuda-repo-ubuntu1404-7-0-local_7.0-28_amd64.deb

7. **install sougou input method for chinese input....poor english...** (**done**)

    *按下Ctrl + space，切换输入法。*

------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------

# 2015-12-17 by zhaoyue

1. 安装开发所需的依赖包
```sh
sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libboost-all-dev libhdf5-serial-dev libgflags-dev libgoogle-glog-dev liblmdb-dev protobuf-compiler #required by caffe    (**done**)
```
------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------

# 2015-12-18 by zhaoyue

1. 上传cudnn包和atlas软件包到/home/renwh/gaze/share目录
2. 安装cuda       (**done**) 
3. 安装cuDNN      (**done**)   更新了etc/profile
4. 安装Atlas （跳过了安装CUDA SAMPLE）      (**done**) 
5. 安装opencv2.4.10                        (**done**) 
6. 安装python2.7 （步骤6.1） 安装目录usr/local/anconda3                         (**done**) 


## .....系统里默认的python是3.5版本，没问题么？PS：陈龙老师服务器上是2.7， 我在问有没有区别。但是建议改成2.7版本，因为，我个人倾向于最后使用python而不是matlab，python3.x版本没怎么用过。。。。。。。要跑RCNN需要Matlab。。。。可能都要装。
##pyhton 这个安装包搞错了，下载的为3.5版本的，已经将原版本删除，更换为2.7版本,2.7版本似乎更加适合caffe


------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------

# 2015-12-19 by Paul W. REN

1. software updater.(**doing**)
    linux-image-3.13.0-74-generic
    linux-image-extra-3.13.0-74-generic
2. bash
```sh
source /etc/profile    **更新了环境变量**
sudo ldconfig          **更新链接库**
```
3. 关机，换电源和显卡(**done**)

4. 安装cuda sample(**done**)

**Result** 

```sh
renwh@renwh-desktop:/usr/local/cuda/samples$ bin/x86_64/linux/release/deviceQuery
bin/x86_64/linux/release/deviceQuery Starting...

CUDA Device Query (Runtime API) version (CUDART static linking)

Detected 1 CUDA Capable device(s)

Device 0: "GeForce GTX TITAN X"
  CUDA Driver Version / Runtime Version          7.5 / 7.0
  CUDA Capability Major/Minor version number:    5.2
  Total amount of global memory:                 12287 MBytes (12884180992 bytes)
  (24) Multiprocessors, (128) CUDA Cores/MP:     3072 CUDA Cores
  GPU Max Clock rate:                            1076 MHz (1.08 GHz)
  Memory Clock rate:                             3505 Mhz
  Memory Bus Width:                              384-bit
  L2 Cache Size:                                 3145728 bytes
  Maximum Texture Dimension Size (x,y,z)         1D=(65536), 2D=(65536, 65536), 3D=(4096, 4096, 4096)
  Maximum Layered 1D Texture Size, (num) layers  1D=(16384), 2048 layers
  Maximum Layered 2D Texture Size, (num) layers  2D=(16384, 16384), 2048 layers
  Total amount of constant memory:               65536 bytes
  Total amount of shared memory per block:       49152 bytes
  Total number of registers available per block: 65536
  Warp size:                                     32
  Maximum number of threads per multiprocessor:  2048
  Maximum number of threads per block:           1024
  Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
  Max dimension size of a grid size    (x,y,z): (2147483647, 65535, 65535)
  Maximum memory pitch:                          2147483647 bytes
  Texture alignment:                             512 bytes
  Concurrent copy and kernel execution:          Yes with 2 copy engine(s)
  Run time limit on kernels:                     Yes
  Integrated GPU sharing Host Memory:            No
  Support host page-locked memory mapping:       Yes
  Alignment requirement for Surfaces:            Yes
  Device has ECC support:                        Disabled
  Device supports Unified Addressing (UVA):      Yes
  Device PCI Domain ID / Bus ID / location ID:   0 / 1 / 0
  Compute Mode:
    < Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >

deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 7.5, CUDA Runtime Version = 7.0, NumDevs = 1, Device0 = GeForce GTX TITAN X
Result = PASS
```


------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------

# 2015-12-20 by zhaoyue

1. 更换python 3.5为python 2.7(**done**)
##修改了.bashrc 文件，添了了lib path，未执行6.2, 6.3
2. 安装matlab2013b（**done**)
##ps：文件好大，估计得下一个上午了
##:已经上传完成明天再进行编译安装吧
3. 编译caffe（**done**)  
   ##编译时报错（好像是protobuf的问题，**已解决**）
```sh
.build_release/src/caffe/proto/caffe.pb.cc: In member function ‘virtual bool caffe::PythonParameter::MergePartialFromCodedStream(google::protobuf::io::CodedInputStream*)’:
.build_release/src/caffe/proto/caffe.pb.cc:18420:63: error: ‘class google::protobuf::io::CodedInputStream’ has no member named ‘ReadTagWithCutoff’
     ::std::pair< ::google::protobuf::uint32, bool> p = input->ReadTagWithCutoff(127);

```sh
##报错已解决，似是是安装选项选择错误，将另份份caffe的makefile进行替换就以以正确编译
##（关于caffe安装的另一份教程：http://www.cnblogs.com/cj695/p/4498270.html）含有protobuf问题

------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------

# 2015-12-22 by zhaoyue

1. 编译caffe1（**done**)  路径(/home/renwh/gaze/zhaoy/caffe-master）
##Ps：这个版本的caffe是只有python接口无matlab接口
```sh
 8 tests from CuDNNNeuronLayerTest/0 (47 ms total)

[----------] Global test environment tear-down
[==========] 1128 tests from 198 test cases ran. (144409 ms total)

···sh
##http://www.aiuxian.com/article/p-2150379.html 从这个网页中看，似乎这个是正常的

2. 安装matlab2013b （位置:usr/local/matlab)（**done**)
##已经将matlab添加到应用里的，可以直接在桌面左上角的application中搜索使用

3. 编译caffe2（**done**)   路径(/home/renwh/gaze/caffe-master）
##这个版本包含python 2.7和matlab R2013b接口
## 编译时使用make all -j2就会报错:

```sh
.build_release/src/caffe/proto/caffe.pb.cc: In member function ‘virtual bool caffe::SigmoidParameter::MergePartialFromCodedStream(google::protobuf::io::CodedInputStream*)’:
.build_release/src/caffe/proto/caffe.pb.cc:19028:63: error: ‘class google::protobuf::io::CodedInputStream’ has no member named ‘ReadTagWithCutoff’
     ::std::pair< ::google::protobuf::uint32, bool> p = input->ReadTagWithCutoff(127);
                                                               ^
.build_release/src/caffe/proto/caffe.pb.cc: In member function ‘virtual bool caffe::SliceParameter::MergePartialFromCodedStream(google::protobuf::io::CodedInputStream*)’:
.build_release/src/caffe/proto/caffe.pb.cc:19263:63: error: ‘class google::protobuf::io::CodedInputStream’ has no member named ‘ReadTagWithCutoff’
     ::std::pair< ::google::protobuf::uint32, bool> p = input->ReadTagWithCutoff(127);

```sh
## 估计是本机不持持这种编译方式，所以换make all，可以顺利编译

##caffe2 make runtest报告
```sh
[       OK ] BenchmarkTest/0.TestTimerConstructor (0 ms)
[----------] 5 tests from BenchmarkTest/0 (600 ms total)

[----------] Global test environment tear-down
[==========] 1128 tests from 198 test cases ran. (143782 ms total)
[  PASSED  ] 1128 tests.

  YOU HAVE 2 DISABLED TESTS

```sh
##搜索了别人的编译效果，都会出现这个报错，而且有人将这个当做编译成功的标志，求问？

##编译Matlab wrapper
```sh
root@renwh-desktop:/home/renwh/gaze/share/caffe-master# make matcaffe
make: brew: Command not found
make: brew: Command not found
**参见：http://brew.sh/  brew是mac-ox 下的安装命令，出现上面的错误，应该是makefile.config文件配置的问题  by REN**
MEX matlab/caffe/matcaffe.cpp

Warning: You are using gcc version "4.8.4".  The version
         currently supported with MEX is "4.7.x".
         For a list of currently supported compilers see: 
         http://www.mathworks.com/support/compilers/current_release/

```sh
##应该是需要将gcc降级（*×已完成×*）
  降级方法：**undone** *只是从网上找到这个方法，我还没给gcc降级*
Ubuntu14.04自带的gcc版本是4.8，MATLAB2014a支持的最高版本为4.7x。因此，需要安装gcc4.7，并给gcc降级

在终端执行gcc 4.7的安装命令：sudo apt-get install gcc-4.7 g++-4.7 g++-4.7-multilib gcc-4.7-multilib

在终端执行以下系统gcc降级命令：sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.7 100 

sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 50 

sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.7 100 

sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 50

sudo update-alternatives --install /usr/bin/cpp cpp-bin /usr/bin/cpp-4.7 100

sudo update-alternatives --install /usr/bin/cpp cpp-bin /usr/bin/cpp-4.8 50

验证gcc-4.7是否安装并成为系统的默认版本：gcc -v 

------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------

# 2015-12-23 by Paul W. REN
1. 从github上下载了最
新版的caffe源码，放在了 ~/gaze/share/caffe-master.zip **建议以后编译用最新的源码，编译的时候，请复制一份源码到自己的目录，在复制的的源码目录编译，不要对原始源码目录做修改。**

2. 根据我的个人理解，配置了一份适用于我们机子的makefile.config，存放在～/gaze/share/Makefile.config.example **PS，最新版的caffe貌似需要cudnn v3而不是，我们装的那个v2版本。所以暂时编译的时候没有添加cudnn支持。**

3. 使用上面的配置文件，在～/gaze/renwh/caffepy/目录下编译caffe

```sh
make all -j2
make test
make runtest
```

输出：
    [----------] Global test environment tear-down
    [==========] 1664 tests from 247 test cases ran. (207685 ms total)
    [  PASSED  ] 1664 tests.

```sh
# renwh@renwh-desktop:~/gaze/renwh/caffepy$ make matcaffe
MEX matlab/+caffe/private/caffe_.cpp

Warning: You are using gcc version "4.8.4".  The version
         currently supported with MEX is "4.7.x".
         For a list of currently supported compilers see: 
         http://www.mathworks.com/support/compilers/current_release/

# renwh@renwh-desktop:~/gaze/renwh/caffepy$ make pycaffe
CXX/LD -o python/caffe/_caffe.so python/caffe/_caffe.cpp
touch python/caffe/proto/__init__.py
PROTOC (python) src/caffe/proto/caffe.proto
```

## 编译最新版caffe源码出现的错误。
1. 最新版的caffe貌似需要cudnn v3而不是，我们装的那个v2版本。所以暂时编译的时候没有添加cudnn支持。
2. 当make rutest时出现.build_release/test/...:error while loading shared libraries:libhdf5_hl.so.8:cannot open shared object file:No such file or directory

原因：最新的caffe支持的hdf5库版本应该升级到v10，我们用的是v7，我直接用软链接解决。希望对之后没影响。
解决方法：cd /usr/lib/x86_64-linux-gnu

    sudo ln -s libhdf5.so.7 libhdf5.so.10

    sudo ln -s libhdf5_hl.so.7 libhdf5_hl.so.10

    sudo ldconfig

------------------------------------------------------------------------------------------------


------------------------------------------------------------------------------------------------

# 2015-12-23 by zhaoyue

1. 建立device&lib.md 文件，用于记录已经安装的软件或lib的信息
2. 更新cudnn为V3版本
3. 重新编译caffe，包含matlab和python接口，使用cudnnV3，cuda7.0（**done**)   
##路径(/home/renwh/gaze/zhaoy/caffe-master）


--------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------

# 2015-12-30 by Paul W. REN
1. 拷贝了两份caffe和CNN的课程资料给大家一起学习。放在了 *~/gaze/share/caffe_cnn公开课* 目录下。

-----------------

------------------------------------------------------------------------------------------------


# 2015-1-3 by zhuyixin
1. 拷贝数据集MPII_data到 *-/gaze/zhuyx
2. 拷贝初步数据处理结果Result 到*-/gaze/zhuyx readme文件位于该目录下

----------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------

# 2015-1-4 by Paul W. REN

1. 从[mpii](http://www.mpi-inf.mpg.de/departments/computer-vision-and-multimodal-computing/research/gaze-based-human-computer-interaction/appearance-based-gaze-estimation-in-the-wild/)下载改进的 *"accuracy" and "euclidean distance" layers of Caffe.* 放在 **~/gaze/share/CaffeLayerModification.zip** 

2. 将修改过的caffe layer文件解压，放在caffe源码目录文件，编译caffe_for_gaze.(需要修改头文件)。

euclidean_loss_layer.cpp修改部分代码如下：

```c

    //#include "caffe/layer.hpp"
    //#include "caffe/util/io.hpp"
    //#include "caffe/util/math_functions.hpp"
    //#include "caffe/vision_layers.hpp"
    #include "caffe/layers/euclidean_loss_layer.hpp"
    #include "caffe/util/math_functions.hpp"

```
euclidean_loss_layer.cu修改部分代码如下：

```c

    //#include "caffe/layer.hpp"
    //#include "caffe/util/io.hpp"
    //#include "caffe/util/math_functions.hpp"
    //#include "caffe/vision_layers.hpp"
    #include "caffe/layers/euclidean_loss_layer.hpp"
    #include "caffe/util/math_functions.hpp"

```
accuracy_layer.cpp修改部分代码如下：

```c

    //#include "caffe/layer.hpp"
    //#include "caffe/util/io.hpp"
    //#include "caffe/util/math_functions.hpp"
    //#include "caffe/vision_layers.hpp"
    #include "caffe/layers/accuracy_layer.hpp"
    #include "caffe/util/math_functions.hpp"

```

3. 编译caffe。

```sh

    make all -j4
    make test -j4
    make runtest

```

make runtest报错：

```sh

    src/caffe/test/test_accuracy_layer.cpp:246: Failure
    The difference between this->blob_top_->data_at(0, 0, 0, 0) and num_correct_labels / 100.0 is 76.721350296078924, which exceeds 1e-4, where
    this->blob_top_->data_at(0, 0, 0, 0) evaluates to 77.021350296078921,
    num_correct_labels / 100.0 evaluates to 0.29999999999999999, and
    1e-4 evaluates to 0.0001.
    [  FAILED  ] AccuracyLayerTest/1.TestForwardCPUTopK, where TypeParam = double (1 ms)
    [ RUN      ] AccuracyLayerTest/1.TestForwardWithSpatialAxes
    F0104 18:15:38.583951 11746 accuracy_layer.cpp:29] Check failed: bottom[1]->height() == 1 (5 vs. 1) 
    *** Check failure stack trace: ***
        @     0x2b79bed0adaa  (unknown)
        @     0x2b79bed0ace4  (unknown)
        @     0x2b79bed0a6e6  (unknown)
        @     0x2b79bed0d687  (unknown)
        @     0x2b79c0f32a2c  caffe::AccuracyLayer<>::Reshape()
        @           0x472bf1  caffe::Layer<>::SetUp()
        @           0x663cf6  caffe::AccuracyLayerTest_TestForwardWithSpatialAxes_Test<>::TestBody()
        @           0x872b0a  testing::internal::HandleExceptionsInMethodIfSupported<>()
        @           0x868179  testing::Test::Run()
        @           0x868257  testing::TestInfo::Run()
        @           0x868395  testing::TestCase::Run()
        @           0x86860d  testing::internal::UnitTestImpl::RunAllTests()
        @           0x87268a  testing::internal::HandleExceptionsInMethodIfSupported<>()
        @           0x8679d1  testing::UnitTest::Run()
        @           0x465342  main
        @     0x2b79c1d26ec5  (unknown)
        @           0x46c1b9  (unknown)
        @              (nil)  (unknown)
    make: *** [runtest] Aborted (core dumped)

4. 安装了ctags。方便读代码。使用方式参看[我的旧blogs](http://blog.csdn.net/paul_c_v/article/details/46430111)



```

----------------------------------------------------------------------------------------------

----------------------------------------------------------------------------------------------

# 2015-12-30 by Paul W. REN

1. 在caffe_root/python 目录下尝试 进入python import caffe 报错。
    Traceback (most recent call last):
      File "test.py", line 1, in <module>
        import caffe
      File "/home/renwh/gaze/renwh/caffe_with_cudnnv3/python/caffe/__init__.py", line 1, in <module>
        from .pycaffe import Net, SGDSolver, NesterovSolver, AdaGradSolver, RMSPropSolver, AdaDeltaSolver, AdamSolver
      File "/home/renwh/gaze/renwh/caffe_with_cudnnv3/python/caffe/pycaffe.py", line 15, in <module>
        import caffe.io
      File "/home/renwh/gaze/renwh/caffe_with_cudnnv3/python/caffe/io.py", line 8, in <module>
        from caffe.proto import caffe_pb2
      File "/home/renwh/gaze/renwh/caffe_with_cudnnv3/python/caffe/proto/caffe_pb2.py", line 4, in <module>
        from google.protobuf.internal import enum_type_wrapper
    ImportError: No module named google.protobuf.internal

**google 得出，是因为Installing 'pip install protobuf' did the trick for me :-)。**

[问题解决链接](https://groups.google.com/forum/#!topic/caffe-users/9Q10WkpCGxs)

**通过检查安装日志，发现问题应该处在安装python依赖库（6.2）上。进入caffe_root/python 目录，运行下面命令安装依赖库.**

```sh
for req in $(cat requirements.txt); do pip install $req; done
```

发现果然报错，好几个依赖库没有按上，其中包括**protobuf（权限问题）**.
**由于使用 Anaconda2 虽然省去了很多下载时间，但是不好解决权限问题，通过咨询徐通，决定改用系统python 。**

2. 取消了**~/.bashrc文件中关于Anaconda2的环境变量的注释，改用系统python。**
3. 安装pip。

```sh
sudo apt-get install python-pip
```
4. 进入caffe_root/python 目录，运行下面命令安装依赖库。

```sh
for req in $(cat requirements.txt); do pip install $req; done
```

**绝大多数依赖库正确安装这次。但是还是有两个安装包（3 scipy,4 scikit-image）安装失败**


      1 Cython>=0.19.2
      2 numpy>=1.7.1
      3 scipy>=0.13.2
      4 scikit-image>=0.9.3
      5 matplotlib>=1.3.1
      6 ipython>=3.0.0
      7 h5py>=2.2.0
      8 leveldb>=0.191
      9 networkx>=1.8.1
     10 nose>=1.3.0
     11 pandas>=0.12.0
     12 python-dateutil>=1.4,<2
     13 protobuf>=2.5.0
     14 python-gflags>=2.0
     15 pyyaml>=3.10
     16 Pillow>=2.3.0
     17 six>=1.1.0



5. 解决**3 scipy,4 scikit-image**安装问题
问题解决[参考链接](https://github.com/scipy/scipy/issues/4102).


```sh
pip install --upgrade pip
sudo  apt-get install gfortran
sudo pip install scipy
sudo pip install scikit-image
```

**全部python依赖安装成功，如下**

```sh
    renwh@renwh-desktop:~/gaze/renwh/caffe_with_cudnnv3/python$ for req in $(cat requirements.txt); do pip install $req; done
    Requirement already satisfied (use --upgrade to upgrade): Cython>=0.19.2 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): numpy>=1.7.1 in /usr/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): scipy>=0.13.2 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): scikit-image>=0.9.3 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): matplotlib>=1.1.0 in /usr/local/lib/python2.7/dist-packages (from scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): six>=1.3 in /usr/lib/python2.7/dist-packages (from scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): networkx>=1.8 in /usr/local/lib/python2.7/dist-packages (from scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): pillow>=1.7.8 in /usr/lib/python2.7/dist-packages (from scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): numpy>=1.6 in /usr/lib/python2.7/dist-packages (from matplotlib>=1.1.0->scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): python-dateutil in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.1.0->scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): pytz in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.1.0->scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): cycler in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.1.0->scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): pyparsing>=1.5.6,!=2.0.0,!=2.0.4 in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.1.0->scikit-image>=0.9.3)
    Requirement already satisfied (use --upgrade to upgrade): decorator>=3.4.0 in /usr/local/lib/python2.7/dist-packages (from networkx>=1.8->scikit-image>=0.9.3)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): matplotlib>=1.3.1 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): numpy>=1.6 in /usr/lib/python2.7/dist-packages (from matplotlib>=1.3.1)
    Requirement already satisfied (use --upgrade to upgrade): python-dateutil in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.3.1)
    Requirement already satisfied (use --upgrade to upgrade): pytz in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.3.1)
    Requirement already satisfied (use --upgrade to upgrade): cycler in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.3.1)
    Requirement already satisfied (use --upgrade to upgrade): pyparsing>=1.5.6,!=2.0.0,!=2.0.4 in /usr/local/lib/python2.7/dist-packages (from matplotlib>=1.3.1)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): ipython>=3.0.0 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): h5py>=2.2.0 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): numpy>=1.6.1 in /usr/lib/python2.7/dist-packages (from h5py>=2.2.0)
    Requirement already satisfied (use --upgrade to upgrade): Cython>=0.17 in /usr/local/lib/python2.7/dist-packages (from h5py>=2.2.0)
    Requirement already satisfied (use --upgrade to upgrade): six in /usr/lib/python2.7/dist-packages (from h5py>=2.2.0)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): leveldb>=0.191 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): networkx>=1.8.1 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): decorator>=3.4.0 in /usr/local/lib/python2.7/dist-packages (from networkx>=1.8.1)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): nose>=1.3.0 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): pandas>=0.12.0 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): python-dateutil in /usr/local/lib/python2.7/dist-packages (from pandas>=0.12.0)
    Requirement already satisfied (use --upgrade to upgrade): pytz>=2011k in /usr/local/lib/python2.7/dist-packages (from pandas>=0.12.0)
    Requirement already satisfied (use --upgrade to upgrade): numpy>=1.7.0 in /usr/lib/python2.7/dist-packages (from pandas>=0.12.0)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): python-dateutil>=1.4,<2 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): protobuf>=2.5.0 in /usr/local/lib/python2.7/dist-packages
    Requirement already satisfied (use --upgrade to upgrade): setuptools in /usr/lib/python2.7/dist-packages (from protobuf>=2.5.0)
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): python-gflags>=2.0 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): pyyaml>=3.10 in /usr/local/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): Pillow>=2.3.0 in /usr/lib/python2.7/dist-packages
    Cleaning up...
    Requirement already satisfied (use --upgrade to upgrade): six>=1.1.0 in /usr/lib/python2.7/dist-packages
    Cleaning up...
```

6. 进入*caffe_with_cudnnv3*目录，重新编译caffe,测试caffe接口。

```sh
make clean
make all -j4
make test -j4
make runtest
make pycaffe
```
终于可以成功 **import caffe** 了！！！！！



----------------------------------------------------------------------------------------------


----------------------------------------------------------------------------------------------

# yyyy-mm-dd by someone

1. for example

-----------------






