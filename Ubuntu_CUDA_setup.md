#Ubuntu14.04系统安装CUDA7.0 --吉泓铭

标签（空格分隔）： cuda

---

##CUDA7.0安装
> 1. [下载离线deb文件](https://developer.nvidia.com/cuda-downloads#linux)
2. 把安装包拷贝至home目录下
3. `sudo dpkg -i cuda-repo-ubuntu1404-7-0-local_7.0-28_amd64.deb`
4. `sudo apt-get update`
5. `sudo apt-get install cuda`
6. root：   `sudo passwd root`
7. `su`
8. 打开文件：`gedit ~/.profile`
9. 最末添加：`export CUDA_HOME=/usr/local/cuda-7.0 `
10. 最末添加：`export LD_LIBRARY_PATH=${CUDA_HOME}/lib64`
11. 最末添加：`PATH=${CUDA_HOME}/bin:${PATH} `
12. 最末添加，保存退出`export PATH`
13. `source ~/.profile`
14. `cd /usr/local/cuda/samples/`
15. `make -j12`
16. 重启
17. `cd /usr/local/cuda/samples/bin/x86_64/linux/release`
18. 打印显卡信息，打印成功则配置成功`./deviceQuery`





