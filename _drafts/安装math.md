==============================================
mathematica
sudo sh Mathematica.sh

激活：
在windows下运行激活程序，填入激活码即可。

安装目录 安装时候提醒

./MathKernel
激活

./mathematica 启动


==============================================
matleb

挂载映像文件
在安装前，把所需文件都拷贝到了xxx目录
使用下列命令挂先行载R2016b_glnxa64_dvd1.iso：
cd ~
mkdir matlab
sudo mount -t auto -o loop <path_doc>/R2016b_glnxa64_dvd1.iso matlab/
安装Matlab
挂载iso之后，会发现文件系统多了一个盘，说明挂载成功，然后进行安装：
sudo <path_doc>/install
**not in matlab dictionary
安装进行到82%的时候，会弹出一个提示框，说请插入dvd2，这时候我们需要重新开一个终端，把dvd2挂载到matlab文件夹中：
sudo mount -t auto -o loop Linux/R2016b_glnxa64_dvd2.iso matlab/
然后在对话框中点击OK，继续安装。完成安装后取消iso挂载：
umount matlab/
sudo rm -r matlab/ #删除空文件夹

激活看教程
