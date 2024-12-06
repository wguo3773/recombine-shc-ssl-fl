# recombine-shc-ssl-fl
SHC-SSL and SHC-FL feature selection algorithms for single cell clustering 

- SHC-SSL (Sparse hierarchial clustering - Spike-and-slab Lasso) and SHC-FL (Sparse hierarchial clustering - Fused Lasso) add SSL and FL penalties to SHC. The SHC penalty is based on a prior distribution of lambda0 and lmabda1 which controls the number of non-zero features. 
- When 𝜆0 → ∞ and 𝜆1 → 0, the SSL penalty = L0-norm penalty; when 𝜆0 = 𝜆1, it is the same as lasso penalty. while lasso constantly biases 𝑤̂𝑗 toward zero, SSL shrinks strongly small 𝑤̂𝑗 ’s toward zeros but only introduces very slight biases for large 𝑤̂𝑗 ’s.! Therefore, it serves as a continuous bridge between L0-norm and lasso penalty.
- we selected the best lambda0 using gap statistic while keeping lamdba1 fixed for SHC-SSL 
- The algorithm iteratively updates U, W, and the posterior θ, ensuring convergence while maintaining the balance between sparsity and feature relevance 

![image](https://github.com/user-attachments/assets/3c9cc624-6066-45db-8158-c167059a2bf2)

We have found that SHC-SSL outperforms both SHC and Seurat in clustering rare cell populations in both simulations and Tabula Sapiens (TS) human single cell transcriptomics datasets 

![image](https://github.com/user-attachments/assets/e588656e-b782-40e7-acba-02c5b2b69a07)

Links to files - 

Slides - https://github.com/wguo3773/recombine-shc-ssl-fl/blob/main/RECOMBINE%20ppt.pptx 

Code (R Markdown) - https://github.com/wguo3773/recombine-shc-ssl-fl/blob/main/RECOMBINE_final_results_WG.html
