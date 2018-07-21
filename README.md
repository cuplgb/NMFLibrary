# NMFLibrary
Matlab library for non-negative matrix factorization (NMF)

Authors: [Hiroyuki Kasai](http://www.kasailab.com/)

Last page update: July 21, 2018

Latest library version: 1.2.0 (see Release notes for more info)

<br />

Introduction
----------
The NMFLibrary is a **pure-Matlab** library of a collection of algorithms of **non-negative matrix factorization (NMF)**. 

<br />

## <a name="supp_solver"> List of the algorithms available in NMFLibrary </a>

- Base NMF
    - **MU** (multiplicative updates)
        - MU
            - D. D. Lee and H. S. Seung, "[Algorithms for non-negative matrix factorization](https://papers.nips.cc/paper/1861-algorithms-for-non-negative-matrix-factorization.pdf)," NIPS 2000.
        - Modified MU
            - C.-J. Lin, "[On the convergence of multiplicative update algorithms for nonnegative matrix factorization](http://ieeexplore.ieee.org/document/4359171/)," IEEE Trans. Neural Netw. vol.18, no.6, pp.1589-1596, 2007. 
        - Acceralated MU
            - N. Gillis and F. Glineur, "[Accelerated multiplicative updates and hierarchical ALS algorithms for nonnegative matrix factorization](https://arxiv.org/pdf/1107.5194.pdf)," Neural Computation, vol.24, no.4, pp. 1085-1105, 2012. 

    - **PGD** (projected gradient descent)
        - PGD
        - Direct PGD
            - C.-J. Lin, "[Projected gradient methods for nonnegative matrix factorization](https://www.csie.ntu.edu.tw/~cjlin/papers/pgradnmf.pdf)," Neural Computation, vol.19, no.10, pp.2756-2779, 2007.

    - **ALS** (alternative least squares)
        - ALS
        - Hierarchical ALS (HALS)
            - A. Cichocki and P. Anh-Huy, "[Fast local algorithms for large scale nonnegative matrix and tensor factorizations](http://www.bsp.brain.riken.jp/publications/2009/Cichocki-Phan-IEICE_col.pdf)," IEICE Trans. on Fundamentals of Electronics, Communications and Computer Sciences, vol.92, no.3, pp. 708-721, 2009.
        - Acceralated Hierarchical ALS
            - N. Gillis and F. Glineur, "[Accelerated multiplicative updates and hierarchical ALS algorithms for nonnegative matrix factorization](https://arxiv.org/pdf/1107.5194.pdf)," Neural Computation, vol.24, no.4, pp. 1085-1105, 2012. 


    - **ANLS** (alternative non-negative least squares)
        - ASGROUP (ANLS with Active Set Method and Column Grouping)
        - ASGIVENS (ANLS with Active Set Method and Givens Updating)
        - BPP (ANLS with Block Principal Pivoting Method)
            - J. Kim, Y. He, and H. Park, "[Algorithms for nonnegative matrix and tensor factorizations: A unified view based on block coordinate descent framework](https://link.springer.com/article/10.1007/s10898-013-0035-4)," Journal of Global Optimization, 58(2), pp. 285-319, 2014.
            - J. Kim and H. Park, "[Fast nonnegative matrix factorization: An active-set-like method and comparisons](http://epubs.siam.org/doi/abs/10.1137/110821172)," SIAM Journal on Scientific Computing (SISC), 33(6), pp. 3261-3281, 2011.

- Online/stochstic NMF

    - **INMF** (Incremental NMF) and **ONMF** (Online NMF)
        - S. S. Bucak and B. Gunsel, "[Incremental Subspace Learning via Non-negative Matrix Factorization](https://www.sciencedirect.com/science/article/pii/S0031320308003725)," Pattern Recognition, 2009.

    - **SPG** (Stochastic projected gradient descent)

    - **RONMF** (Robust online NMF)
        - R. Zhao and Y. F. Tan, "[Online nonnegative matrix factorization with outliers](https://ieeexplore.ieee.org/document/7676413/)," IEEE ICASSP2016, 2016.

    - **SAGA-MU-NMF** (SAGA multiplicative updates)
        - R. Serizel, S. Essid and G.Richard, "[Mini-batch stochastic approaches for accelerated multiplicative updates in nonnegative matrix factorisation with beta-divergence](https://ieeexplore.ieee.org/document/7738818/),", IEEE 26th International Workshop on Machine Learning for Signal Processing (MLSP), 2016.

    - **SMU** (Stochastic multiplicative updates) and **SVRMU** (Stochastic variance reduced multiplicative updates)
        - H. Kasai, "[Stochastic variance reduced multiplicative update for nonnegative matrix factorization](https://arxiv.org/abs/1710.10781)," IEEE ICASSP2018, 2018.

- Robust NMF

- Else

    - **GNMF** (Graph Regularized NMF)
        - D. Cai, X. He, X. Wu, and J. Han, "[Non-negative Matrix Factorization on Manifold](https://ieeexplore.ieee.org/document/4781101/)," Proc. 2008 Int. Conf. on Data Mining (ICDM), 2008. 
        - D. Cai, X. He, J. Han and T. Huang, "[Graph Regularized Non-negative Matrix Factorization for Data Representation](https://ieeexplore.ieee.org/document/5674058/)," IEEE Transactions on Pattern Analysis and Machine Intelligence, Vol.33, No.8, pp.1548-1560, 2011. 

    - **Semi-NMF** 
        - C.H.Q. Ding, T. Li, M. I. Jordan, "[Convex and Semi-Nonnegative Matrix Factorizations](https://ieeexplore.ieee.org/document/4685898/)," IEEE Transactions on Pattern Analysis and Machine Intelligence, vol.32, no.1, 2010. 

    - **SDNMF** (NMF with Sinkhorn Distance)
        - W. Qian, B. Hong, D. Cai, X. He, and X. Li, "Non-negative Matrix Factorization with Sinkhorn Distance", IJCAI, pp.1960-1966, 2016.
    

<br />

## Algorithm configurations


|Algorithm name in example codes| function | `options.alg` | other `options` |
|---|---|---|---|
|MU|`nmf_mu`|`mu`||
|Modified MU|`nmf_mu`|`mod_mu`||
|Acceralated MU|`nmf_mu`|`acc_mu`||
|PGD|`nmf_pgd`|`pgd`||
|Direct PGD|`nmf_pgd`|`direct_pgd`||
|ALS|`nmf_als`|`als`||
|Hierarchical ALS|`nmf_als`|`hals_mu`||
|Acceralated hierarchical ALS|`nmf_als`|`acc_hals_mu`||
|ASGROUP|`nmf_anls`|`anls_asgroup`||
|ASGIVENS|`nmf_anls`|`anls_asgivens`||
|BPP|`nmf_anls`|`anls_bpp`||
|GNMF|`GNMF`|||
|Semi-NMF|`semi_nmf`|||
|SDNMF|`SDNMF`|||
|SMU|`smu_nmf`|||
|SVRMU|`svrmu_nmf`|||


<br />

Folders and files
---------
<pre>
./                      - Top directory.
./README.md             - This readme file.
./run_me_first.m        - The scipt that you need to run first.
./demo.m                - Demonstration script to check and understand this package easily. 
./demo_face.m           - Demonstration script to check and understand this package easily. 
|plotter/               - Contains plotting tools to show convergence results and various plots.
|auxiliary/             - Some auxiliary tools for this project.
|solver/                - Contains various optimization algorithms.
    |--- base/          - Basic NMF solvers.
    |--- online/        - Online/stochstic NMF solvers.
    |--- robust/        - Robust NMF solvers.
    |--- 3rd_party/     - Solvers provided by 3rd_party.
</pre>

<br />                              

First to do
----------------------------
Run `run_me_first` for path configurations. 
```Matlab
%% First run the setup script
run_me_first; 
```

<br />

Simplest usage example: 4 steps!
----------------------------

Just execute `demo` for the simplest demonstration of this package. .

```Matlab
%% Execute the demonstration script
demo; 
```

The "**demo.m**" file contains below.
```Matlab
%% generate synthetic data non-negative matrix V size of (mxn)
m = 500;
n = 100;
V = rand(m,n);
    
%% Initialize rank to be factorized
rank = 5;

%% perform factroization
% MU
options.alg = 'mu';
[w_nmf_mu, infos_nmf_mu] = nmf_mu(V, rank, options);
% Hierarchical ALS
options.alg = 'hals';
[w_nmf_hals, infos_nmf_hals] = nmf_als(V, rank, options);        
    
%% plot
display_graph('epoch','cost', {'MU', 'HALS'}, {w_nmf_mu, w_nmf_hals}, {infos_nmf_mu, infos_nmf_hals});

```

<br />

Let's take a closer look at the code above bit by bit. The procedure has only **4 steps**!
<br />

**Step 1: Generate data**

First, we generate  synthetic data of V of size (mxn).
```Matlab    
m = 500;
n = 100;
V = rand(m,n);
```

**Step 2: Define rank**

We set the rank value.
```Matlab
rank = 5;
```

**Step 3: Perform solver**

Now, you can perform optimization solvers, e.g., MU and Hierarchical ALS (HALS), calling [solver functions](#supp_solver), i.e., `nmf_mu()` function and `nmf_als()` function after setting some optimization options. 
```Matlab
% MU
options.alg = 'mu';
[w_nmf_mu, infos_nmf_mu] = nmf_mu(V, rank, options);
% Hierarchical ALS
options.alg = 'hals';
[w_nmf_hals, infos_nmf_hals] = nmf_als(V, rank, options); 
```
They return the final solutions of `w` and the statistics information that include the histories of epoch numbers, cost values, norms of gradient, the number of gradient evaluations and so on.

**Step 4: Show result**

Finally, `display_graph()` provides output results of decreasing behavior of the cost values in terms of the number of iterrations (epochs) and time [sec]. 
```Matlab
display_graph('epoch','cost', {'MU', 'HALS'}, {w_nmf_mu, w_nmf_hals}, {infos_nmf_mu, infos_nmf_hals});
display_graph('time','cost', {'MU', 'HALS'}, {w_nmf_mu, w_nmf_hals}, {infos_nmf_mu, infos_nmf_hals});
```

That's it!


<img src="http://www.kasailab.com/public/github/NMFLibrary/images/cost.png" width="600">

<br />

More plots
----------------------------

"**demo_face.m**" illustrates the learned basis (dictrionary) in case of [CBCL face datasets](http://cbcl.mit.edu/software-datasets/FaceData2.html).

The dataset is first loaded into V instead of generating synthetic data in **Step 1**.

```Matlab
V = importdata('./data/CBCL_face.mat');
```

Then, we can display basis elements (W: dictionary) obtained with different algorithms additionally in **Step 4**.

```Matlab
plot_dictionnary(w_nmf_mu.W, [], [7 7]); 
plot_dictionnary(w_nmf_hals.W, [], [7 7]); 
```

<img src="http://www.kasailab.com/public/github/NMFLibrary/images/face_dictionary.png" width="600">


<br />

License
-------
- The NMFLibrary is **free**, **non-commercial** and **open** source.
- The code provided iin NMFLibrary should only be used for **academic/research purposes**.
- Third party files are included.
    - For ANLS algorithms: `nnlsm_activeset.m`, `nnls1_asgivens.m`, `nnlsm_blockpivot.m`, and `normalEqComb.m` written by Jingu Kim.
    - For PGD algorithm: `nlssubprob.m`.
    - For GNMF algorith: `GNMF.m`, `GNMF_Multi.m`, `constructW.m` and `litekmeans.m` writtnen by Deng Cai.
    - For SDNMF algorith: `SDNMF.m`, and `SDNMF_Multi.m` writtnen by Wei Qian.
    - For acceleration sub-routines in [`nmf_mu.m`](https://github.com/hiroyuki-kasai/NMFLibrary/blob/master/solver/base/nmf_mu.m) and [`nmf_als.m`](https://github.com/hiroyuki-kasai/NMFLibrary/blob/master/solver/base/nmf_als.m) for MU and HALS from [Nicolas Gillis](https://sites.google.com/site/nicolasgillis/publications).
    - For dictionaly visualization: `plot_dictionnary.m`, `rescale.m`, and `getoptions.m`.


<br />

Problems or questions
---------------------
If you have any problems or questions, please contact the author: [Hiroyuki Kasai](http://kasai.kasailab.com/) (email: kasai **at** is **dot** uec **dot** ac **dot** jp)

<br />

Release notes
--------------
* Version 1.2.0 (Jul. 21, 2018)
    - GNMF, Semi-NMF and SDNMF are added.
* Version 1.1.0 (Apr. 17, 2018)
    - Online/stochastic solvers are added.
* Version 1.0.0 (Apr. 04, 2017)
    - Initial version.

