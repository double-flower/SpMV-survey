<div align="center">
  <h2><i>A Systematic Survey of Sparse Matrix Vector Multiplication</i></h2> 
</div>

<div align="center">
<b>Jianhua Gao</b><sup>1</sup>,
<b>Bingjie Liu</b><sup>2</sup>,
<b>Weixing Ji</b><sup>1</sup>,
<b>Hua Huang</b><sup>1</sup>
</div>

<div align="center">
<sup>1</sup>School of Artificial Intelligence, Beijing Normal University
</div>
<div align="center">
<sup>2</sup>School of Computer Science and Technology, Beijing Institute of Technology
</div>

We present a systematic survey of sparse matrix-vector multiplication (SpMV).

## Content
- [Papers](#papers)
  - [Survey](#survey)
  - [Sparse Compression Formats](#sparse-compression-formats)
  - [Auto-Tuning Based Algorithm](auto-tuning-based-algorithm)
  - [Machine-Learning Based Algorithm](machine-learning-based-algorithm)
  - [Mixed Precision Based Optimization](#mixed-Precision-based-optimization)
  - [Architecture Oriented Optimization](#architecture-oriented-optimization)

  
- [Citation](#citation)


## Survey
- **A Survey on Performance Modelling and Optimization Techniques for SpMV on GPUs**. *Ms. Aditi V. Kulkarni, Prof. C. R. Barde. International Journal of Computer Science and Information Technologies (IJCSIT), 2014* [[pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=eeb465ba9655a5a0c638e15fe2421c5d9a708d46)] ![](https://img.shields.io/badge/Arxiv2014-orange)
- **A Survey of Sparse Matrix-Vector Multiplication Performance on Large Matrices**. *Max Grossman, Christopher Thiele, Mauricio Araya-Polo, Florian Frank, Faruk O. Alpak, Vivek Sarkar. arXiv, 2016* [[pdf](https://arxiv.org/pdf/1608.00636)] ![](https://img.shields.io/badge/Arxiv2016-orange)
- **Sparse Matrix-Vector Multiplication on GPGPUs**. *Salvatore Filippone, Valeria Cardellini, Davide Barbieri, Alessandro Fanfarillo. ACM Transactions on Mathematical Software (TOMS), 2017* [[DOI](https://dl.acm.org/doi/10.1145/3017994)]
- **Research on Performance Optimization for Sparse Matrix-Vector Multiplication in Multi/Many-core Architecture**. *Qihan Wang, Mingliang Li, Jianming Pang, Di Zhu. in 2020 2nd International Conference on Information Technology and Computer Application (ITCA). IEEE, 2020* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9422076)] ![](https://img.shields.io/badge/ITCA2020-orange)
- **A Survey of Accelerating Parallel Sparse Linear Algebra**. *Guoqing Xiao, Chuanghui Yin, Tao Zhou, Xueqi Li, Yuedan Chen, Kenli Li. ACM Computing Surveys, 2023* [[DOI](https://dl.acm.org/doi/10.1145/3604606)]
- **A Survey on Performance Modelling and Optimization Techniques for SpMV on GPUs**. *Ms. Aditi V. Kulkarni, Prof. C. R. Barde. International Journal of Computer Science and Information Technologies (IJCSIT),2014* [[pdf](https://www.ijcsit.com/docs/Volume%205/vol5issue06/ijcsit20140506146.pdf)]
- **Graph Processing on GPUs: A Survey**. *X. Shi, Z. Zheng, Y. Zhou, H. Jin, L. He, B. Liu, and Q. Hua. ACM Comput. Surv., vol. 50, no. 6, 2018* [[pdf](https://www.dcs.warwick.ac.uk/~liganghe/papers/ACM-Computing-Surveys-2017.pdf)]
  
## Sparse Compression Formats
### Basic Compression Formats
- **Data structures to vectorize CG algorithms for general sparsity patterns**. *Gaia Valeria Paolini, Giuseppe Radicati Di Brozolo. BIT Numerical Mathematics(BIT Numer. Math), 1989* [[DOI](https://link.springer.com/article/10.1007/BF01932741)]
- **Sparse matrix vector multiplication techniques on the IBM 3090 VF**. *A. Peters. Parallel Computing, 1991* [[DOI](https://www.sciencedirect.com/science/article/abs/pii/S0167819105800079)]
- **SPARSKIT: A Basic Took Kit for Sparse Matrix Computations, Version 2**. *Youcef Saad. 1994* [[pdf](https://www.finley-lab.com/files/gau19/exercises/exercise-sparskit/sparskit-v2.pdf)]
- **Scan Primitives for GPU Computing**. *Shubhabrata Sengupta, Mark Harris, Yao Zhang, John D. Owens. in Proceedings of the 22nd ACM SIGGRAPH/EUROGRAPHICS Symposium, 2007* [[pdf](https://escholarship.org/content/qt8051p6nd/qt8051p6nd_noSplash_cdf4d7488f42df951707ca97e860123f.pdf)]
- **Sparse Matrix Computations on Manycore GPU’s**. *Michael Garland. in Proceedings of the 45th annual Design Automation Conference, 2008* [[pdf]([https://dl.acm.org/doi/abs/10.1145/1391469.1391473](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4555771))]

### New Compression Formats

#### Regular Slicing

#### Regular Blocking

#### Irregular Compressing

#### Bit/Byte Compressing

#### Hybrid Encoding

#### Other variants

## Auto-Tuning Based Algorithm

### Offline Auto-Tuning

### Online Auto-Tuning


## Machine-Learning Based Algorithm
### Format or Algorithm Selection
- **Random walk with restart: fast solutions and applications**. *H. Tong, C. Faloutsos, and J. Pan.Knowl. Inf. Syst., vol. 14, no. 3, 2008* [[pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=9ebf0f5f36d1504e96d147f38e5b9e21d7d28825)]
- **Authoritative sources in a hyperlinked environment**. *J. M. Kleinberg, J. ACM, vol. 46, no. 5, 1999* [[pdf](https://dl.acm.org/doi/pdf/10.1145/324133.324140)]
- **Reprint of: The anatomy of a large-scale hypertextual web search engine**. *S. Brin and L. Page, Comput. Networks, vol. 56, no. 18, 2012* [[website](https://www.sciencedirect.com/science/article/abs/pii/S1389128612003611)]
### Parameter Prediction

### Performance Prediction

## Mixed Precision Based Optimization

### Mixed-Precision SpMV

### Mixed-Precision SpMV

## Architecture Oriented Optimization
### CPU
- **Data structures to vectorize cg algorithms for general sparsity patterns**. *G. V. Paolini and G. R. D. Brozolo, BIT Numerical Mathematics, vol. 29, no. 4, 1989* [[website](https://link.springer.com/article/10.1007/BF01932741)]


### GPU
#### Single GPU
- **Fast sparse matrix-vector multiplication on gpus for graph applications**. *A. Ashari, N. Sedaghati, J. Eisenlohr, S. Parthasarathy, and P. Sadayappan. in International Conference for High Performance Computing, Networking, Storage and Analysis, SC 2014, New Orleans, LA, USA, November 16-21, 2014, T. Damkroger and J. J. Dongarra, Eds. IEEE Computer Society, 2014* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7013051)]
- **Efficient pagerank and spmv computation on AMD gpus**. *T. Wu, B. Wang, Y. Shan, F. Yan, Y. Wang, and N. Xu. in 39th International Conference on Parallel Processing, ICPP 2010, San Diego, California, USA, 13-16 September 2010. IEEE Computer Society, 2010* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5599152)]
- **Implementing Sparse Matrix-Vector Multiplication on Throughput-Oriented Processors**. *N. Bell and M. Garland. in Proceedings of the ACM/IEEE Conference on High Performance Computing, SC, November 14-20, 2009, Portland, Oregon, USA. ACM, 2009* [[pdf](https://www.mgarland.org/files/papers/sc09-spmv-throughput.pdf)]
  
#### Multiple GPU

### FPGA

### Processing in Memory

### Heterogeneous Platform

### Distributed Platform

