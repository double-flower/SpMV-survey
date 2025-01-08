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
- **Graph Processing on GPUs: A Survey**. *X. Shi, Z. Zheng, Y. Zhou, H. Jin, L. He, B. Liu, and Q. Hua. ACM Comput. Surv., vol. 50, no. 6, 2018* [[pdf](https://www.dcs.warwick.ac.uk/~liganghe/papers/ACM-Computing-Surveys-2017.pdf)]
  
## Sparse Compression Formats
### Basic Compression Formats

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
- **Random walk with restart: fast solutions and applications**. *H. Tong, C. Faloutsos, and J. Pan.Knowl. Inf. Syst., vol. 14, no. 3, 2008* [[pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=9ebf0f5f36d1504e96d147f38e5b9e21d7d28825)]
### Format or Algorithm Selection

### Parameter Prediction

### Performance Prediction

## Mixed Precision Based Optimization

### Mixed-Precision SpMV

### Mixed-Precision SpMV

## Architecture Oriented Optimization
### CPU
- **Research on Performance Optimization for Sparse Matrix-Vector Multiplication in Multi/Many-core Architecture**. *Q. Wang, M. Li, J. Pang, and D. Zhu. in 2020 2nd International Conference on Information Technology and Computer Application (ITCA). IEEE, 2020* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9422076)]

### GPU
#### Single GPU
- **Fast sparse matrix-vector multiplication on gpus for graph applications**. *A. Ashari, N. Sedaghati, J. Eisenlohr, S. Parthasarathy, and P. Sadayappan. in International Conference for High Performance Computing, Networking, Storage and Analysis, SC 2014, New Orleans, LA, USA, November 16-21, 2014, T. Damkroger and J. J. Dongarra, Eds. IEEE Computer Society, 2014* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7013051)]
- **Efficient pagerank and spmv computation on AMD gpus**. *T. Wu, B. Wang, Y. Shan, F. Yan, Y. Wang, and N. Xu. in 39th International Conference on Parallel Processing, ICPP 2010, San Diego, California, USA, 13-16 September 2010. IEEE Computer Society, 2010* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5599152)]
#### Multiple GPU

### FPGA

### Processing in Memory

### Heterogeneous Platform
- **PanguLU: A Scalable Regular Two-Dimensional Block-Cyclic Sparse Direct Solver on Distributed Heterogeneous Systems**. *X. Fu, B. Zhang, T. Wang, W. Li, Y. Lu, E. Yi, J. Zhao,
X. Geng, F. Li, J. Zhang, Z. Jin, and W. Liu. in Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis, SC 2023, Denver, CO, USA, November 12-17, 2023, D. Arnold, R. M. Badia, and K. M. Mohror, Eds. ACM, 2023* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10485129)]

### Distributed Platform

