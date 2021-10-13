## 欢迎

打开[bilibili](https://www.bilibili.com/) 享受美好生活

或者打开[Scopus](https://www.scopus.com/search/form.uri?zone=TopNavBar&origin=resultslist&display=basic#basic)、[科学网](https://www.webofscience.com/wos/alldb/basic-search)来看看文献

或者学习一些有用的知识：

[数电](https://www.bilibili.com/video/BV18p411Z7ce?from=search&seid=15000188297364473279&spm_id_from=333.337.0.0)

[nextnano](https://www.nextnano.com/manual/getting_started.html)

[vasp](https://www.bigbrosci.com/)

[vaspkit](https://tamaswells.github.io/VASPKIT_manual/manual0.73/vaspkit-manual-0.73.html)

[半导体物理](http://mooc1.chaoxing.com/nodedetailcontroller/visitnodedetail?courseId=99784531&knowledgeId=99784645)

[3dmax入门](https://www.bilibili.com/video/BV19W411i7fG?p=1)

[3dmax应用](https://space.bilibili.com/26665449?spm_id_from=333.788.b_765f7570696e666f.1)

### vasp笔记-通过mpi并行计算PBE泛函能带

依次运行如下代码
```通过mpi并行计算PBE泛函能带
ulimit -s unlimited 
source  /opt/intel/parallel_studio_xe_2018.3.051/psxevars.sh intel64
mpirun -np 48 /opt/vasp/vasp.5.4.4/bin/vasp_std
## -np 48 代表并行核数，数值可调整，一般不超过96，本组服务器共192核
##通过vaspkit 108生成静态INCAR、vaspkit 3生成KPOINTS后
cp -f KPATH.in KPOINTS

```
vasp主要运用密度泛函理论（DFT）计算电子体系的能量，由于DFT计算的局限性，vasp最多同时处理10000个电子，难以处理上千原子的巨大体系，尤其难以处理不规则巨型原子团，在运用vasp计算时，要构建好primitive cell & superlattice，并控制好晶格常数和原子数量。除了vasp，CP2K Linear Scaling Self Consistent Field Method和BigDFT等更适合进行上千甚至上万原子体系的计算，但是动辄数百行的INPUT使得入门极其困难，非专业量化计算人士只能望洋兴叹。或许有一天，有人开发出性能强大的多体理论模拟计算软件呢。也可以期待一手量子计算机的普及，实在是一劳永逸解决第一性原理计算的好方法。


### 联系方式

E-mail：13255546653@163.com、21213010014@m.fudan.edu.cn

QQ:995437678

感谢关注

