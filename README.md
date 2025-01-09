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
- **Sparse Matrix-Vector Multiplication on GPGPUs**. *Salvatore Filippone, Valeria Cardellini, Davide Barbieri, Alessandro Fanfarillo. ACM Transactions on Mathematical Software (TOMS), 2017* [[DOI](https://dl.acm.org/doi/10.1145/3017994)] ![](https://img.shields.io/badge/TOMS2017-orange)
- **Research on Performance Optimization for Sparse Matrix-Vector Multiplication in Multi/Many-core Architecture**. *Qihan Wang, Mingliang Li, Jianming Pang, Di Zhu. in 2020 2nd International Conference on Information Technology and Computer Application (ITCA). IEEE, 2020* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9422076)] ![](https://img.shields.io/badge/ITCA2020-orange)
- **A Survey of Accelerating Parallel Sparse Linear Algebra**. *Guoqing Xiao, Chuanghui Yin, Tao Zhou, Xueqi Li, Yuedan Chen, Kenli Li. ACM Computing Surveys, 2023* [[DOI](https://dl.acm.org/doi/10.1145/3604606)]
- **A Survey on Performance Modelling and Optimization Techniques for SpMV on GPUs**. *Ms. Aditi V. Kulkarni, Prof. C. R. Barde. International Journal of Computer Science and Information Technologies (IJCSIT),2014* [[pdf](https://www.ijcsit.com/docs/Volume%205/vol5issue06/ijcsit20140506146.pdf)] ![](https://img.shields.io/badge/IJCSIT2014-orange)
  
## Sparse Compression Formats
### Basic Compression Formats
- **Data structures to vectorize CG algorithms for general sparsity patterns**. *Gaia Valeria Paolini, Giuseppe Radicati Di Brozolo. BIT Numerical Mathematics(BIT Numer. Math), 1989* [[DOI](https://link.springer.com/article/10.1007/BF01932741)]
- **Sparse matrix vector multiplication techniques on the IBM 3090 VF**. *A. Peters. Parallel Computing, 1991* [[DOI](https://www.sciencedirect.com/science/article/abs/pii/S0167819105800079)]
- **SPARSKIT: A Basic Took Kit for Sparse Matrix Computations, Version 2**. *Youcef Saad. 1994* [[pdf](https://www.finley-lab.com/files/gau19/exercises/exercise-sparskit/sparskit-v2.pdf)]
- **Scan Primitives for GPU Computing**. *Shubhabrata Sengupta, Mark Harris, Yao Zhang, John D. Owens. in Proceedings of the 22nd ACM SIGGRAPH/EUROGRAPHICS Symposium, 2007* [[pdf](https://escholarship.org/content/qt8051p6nd/qt8051p6nd_noSplash_cdf4d7488f42df951707ca97e860123f.pdf)]
- **Sparse Matrix Computations on Manycore GPU’s**. *Michael Garland. in Proceedings of the 45th annual Design Automation Conference, 2008* [[pdf]([https://dl.acm.org/doi/abs/10.1145/1391469.1391473](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4555771))]

### New Compression Formats

#### Regular Slicing
- **The Sliced COO Format for Sparse Matrix-Vector Multiplication on CUDA-enabled GPUs**. *Hoang-Vu Dang, Bertil Schmidt. Proceedings of the International Conference on Computational Science(ICCS), 2012* [[pdf](https://pdf.sciencedirectassets.com/280203/1-s2.0-S1877050912X00036/1-s2.0-S1877050912001287/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEKD%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIA3mbg38oZkOfdwWyUCXm1t1E87ZEM34vjwWVr9wgRFZAiEAqFP8FbkBYfhel7NqcTYt%2BxqNVTXQRQOUvhB%2FUAAF2M4qugUIif%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAFGgwwNTkwMDM1NDY4NjUiDGUJGG%2FttwUgdR%2BZpyqOBURWdhDppaUWBl1iQ6%2FfYJSMYpHqrFgsxfVSDaoJQX%2F6DXUEGuV9vMR2M1jtNj%2FMIhRtpGkDmM300CIDtYtxk1GMaUoY%2BR50tF7loJQU9s2fEXXNDs4WflLwkS8lzufV5liMWbHj8tXq7EbIOQ9R6QE9dIThpxv2e4e9RofhPO6%2BbnfPlLKKpI%2FSfLNXRMpwfaeSdjkxdAWWr7omtVwL5IEmpk7tQjad6RBH9bcUcpElapd9umqlwEHBVHRRTMN9wJhGnIWM%2BnljropWr2jSv30x2KinhiG36qYswV7PaeH9Q%2FwJ7QEqWml4WXBM8FITER4PYUxkMsxKYf8vYGUr4p7mIi0P3RZCh%2FbuUwncRTy2akhC3Vx7PnHJqopfR%2BsbRkmiA6lRanbQQQQukP35VAV%2FT1w%2BcxOHWGVjzbKfb80EYVjTAAEwJrlxc8u2iCUWuWRyJqlqwb7LGFTDSFz4PEFXDfS3%2BOEQOBqu3VD%2Bc5WYowxo1X3Snz9ToI5gWqloik0K6ZxwH8ds0J%2B0jAc0yspxdY5kidNkx55enTFen6%2F417K1u1tPnc5slSYaFBWPZGR55v5XzLMEtzwaPCYShXGdZtIFtrYie7tpmJVCUr0DCxH3ZOoobP74nDTnChRUXZA8veCjH4o%2F%2FoGDWHRhFehpvK0qTVqUJ7SYCgZ45PV3077RK1q0o6htw3qJeUDl75ceJVQOyQ3J%2B1%2BtdVAu53dWxO403sYYZ1j0sRGRuUEV0DiDHRqJLL3huwHcjHnVgMjNpkaayidPF08pDWUNHh0YqQE5%2FybD5nVAFhja3%2F%2BiIHHtgri8hk%2F9JQ4KFwMtrb4bKl%2F1SntZoaml2bVaWSxPL8PJyiVBrtVIWSXNwTCe9P27BjqxAc3Fjo%2FzcZYTznWVgDcmTlVKta%2FoSRX%2BuH3WEKUL%2BnOjf7Zqi%2FB6iC%2FUdIbIkug%2B9CHYfooIOiT5fKEwQ2pkO%2B9MYhxfAvWhiD9gPsYfIw2w3Cc7T22PuZUUdO3NpDn9ti3%2Fk8TsHjVF7YEXpm%2F6smdNjVcR1ffgXe1pCNRR%2BwJpRv28krWld8XUEHD5yvuFlO%2FFDWLj%2BOAS3H4VY3QzPgixlLlTMn0%2FVrFoeMZkDdcyFg%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250109T074539Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYXJTEVK4U%2F20250109%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=0281f374273b55135056280db7813d1603678c33327f40cc29bc2acc2bb55030&hash=20fb158082664c615df16bf0d28a6077efd0c915c56fb9409ddf7ca2e72af0db&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1877050912001287&tid=spdf-bc42b010-b5cd-4e6f-ac74-dc8faddb6e25&sid=9dd20b14652bc94e2f281be53321891cc2e0gxrqa&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=0a0e59030454020154&rr=8ff2cf193ae006fa&cc=hk&kca=eyJrZXkiOiJBdDZ2UzcrVU0wQytudk9SNVFGZWNySTh6YThpZjZvYnJTVjIxU0FGdVR3amQzRjJ0Z3Z2a3g1MG5GNlRXS3JzODJob09DY0hUZGUxRi9HcjBpeVNzNUNIRHJTRjA4TnMya2l3bmcxbzRGcnBFMXNlQk4xNUhyYU9WTFVobGNnQUlncXpjZFBDQThoNU1Cek9NTnpmajlnYTNmcHlQcWg3bFlnVUFNYzdkTUlzWXhKViIsIml2IjoiOTgyYzVkNGY1ZjUwMzcxZjkxMjgwMzI1MThiMDdiMGUifQ==_1736408746540)] ![](https://img.shields.io/badge/ICCS2012-orange)
- **Vectorized Sparse Matrix Multiply for Compressed Row Storage Format**. *Eduardo F. D’Azevedo, Mark R. Fahey, Richard T. Mills. Computational Science(ICCS), 2005* [[DOI](https://link.springer.com/chapter/10.1007/11428831_13#preview)] ![](https://img.shields.io/badge/ICCS2005-orange)
- **Automatically Tuning Sparse Matrix-Vector Multiplication for GPU Architectures**. *Alexander Monakov, Anton Lokhmotov, Arutyun Avetisyan. High Performance Embedded Architectures and Compilers(HiPEAC), 2010* [[DOI](https://link.springer.com/chapter/10.1007/978-3-642-11515-8_10)] ![](https://img.shields.io/badge/HiPEAC2010-orange)
- **Three Storage Formats for Sparse Matrices on GPGPUs**. *Davide Barbieri, Alessandro Fanfarillo, Valeria Cardellini, Salvatore Filippone. Technical Report RR-15.6, 2015* [[pdf](https://art.torvergata.it/bitstream/2108/113393/1/DICII-RR-15.6.pdf)] ![](https://img.shields.io/badge/Arxiv2015-orange)
- **Sparse Matrix-vector Multiplication on GPGPU Clusters: A New Storage Format and a Scalable Implementation**. *Moritz Kreutzer, Georg Hager, Gerhard Wellein, Holger Fehske, Achim Basermann, Alan R. Bishop. 26th IEEE International Parallel and Distributed Processing Symposium(IPDPS), 2012* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6270844)] ![](https://img.shields.io/badge/IPDPS2012-orange)
- **A Unified Sparse Matrix Data Format for Efficient General Sparse Matrix-Vector Multiplication on Modern Processors with Wide SIMD Units**. *Moritz Kreutzer, Georg Hager, Gerhard Wellein, Holger Fehske, Alan R. Bishop. SIAM Journal on Scientific Computing(IPDPS), 2014* [[DIO](https://dl.acm.org/doi/abs/10.1137/130930352)] ![](https://img.shields.io/badge/IPDPS2014-orange)
- **Optimizing Sparse Matrix Vector Multiplication Using Diagonal Storage Matrix Format**. *Liang Yuan, Yunquan Zhang, Xiangzheng Sun, Ting Wang.The International Conference on High Performance Computing (HiPC),2010* [[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5581440)] ![](https://img.shields.io/badge/HiPC2010-orange)
- **CRSD: Application Specific Auto-tuning of SpMV for Diagonal Sparse Matrices**. *Xiangzheng Sun, Yunquan Zhang, Ting Wang, Guoping Long, Xianyi Zhang, Yan Li. Euro-Par 2011 Parallel Processing (Euro-Par), 2011* [[DOI](https://link.springer.com/chapter/10.1007/978-3-642-23397-5_32)] ![](https://img.shields.io/badge/Euro-Par2011-orange)

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

