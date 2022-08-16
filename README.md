# initialDegenerationsFlagVarieties

This repository contains the code used in the paper *Initial degenerations of flag varieties* by Daniel Corey and Jorge Alberto Olarte, <a href="https://arxiv.org/abs/2207.08094">arXiv:2207.08094</a>. We use <a href="https://github.com/oscar-system/Polymake.jl" >polymake</a> and <a href="https://github.com/oscar-system/Oscar.jl" >OSCAR</a>, and it works with version 0.10.0. 

```flagMatroids.ipynb``` is a jupyter notebook that generates all flag matroids of rank $(1,2,3)$ on $[4]$. 

```FansOnTFl4.ipynb``` is a jupyter notebook that contains the data of $\operatorname{TF\ell}^{\circ}((1,2,3),4)$. It records the fiber-fan structure (which coincides with the G"obner fan structure computed by ```gfan```), together with all the matroid subdivisions, and the coarsest fan structure. It also contains a verification of Lemma 7.1.   
