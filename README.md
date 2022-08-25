# initialDegenerationsFlagVarieties

This repository contains the code used in the paper *Initial degenerations of flag varieties* by Daniel Corey and Jorge Alberto Olarte, <a href="https://arxiv.org/abs/2207.08094">arXiv:2207.08094</a>. We use <a href="https://github.com/oscar-system/Polymake.jl" >polymake</a> and <a href="https://github.com/oscar-system/Oscar.jl" >OSCAR</a>, and it works with version 0.10.1. 

```flagMatroids.ipynb``` is a jupyter notebook that generates all flag matroids of rank $(1,2,3)$ on $[4]$. 

```FansOnTFl4.ipynb``` is a jupyter notebook that contains the data of $\operatorname{TF\ell}^{\circ}((1,2,3),4)$. It records the fiber-fan structure (which coincides with the G"obner fan structure computed by ```gfan```), together with all the matroid subdivisions, and the coarsest fan structure. It also contains a verification of Lemma 7.1.   

We also have files used to compute $\operatorname{TF\ell}^{\circ}((1,2,3),4)$ with <a href="https://users-math.au.dk/jensen/software/gfan/gfan.html" >gfan</a>. First, run

```gfan_tropicalstartingcone < Fl_123_4_lex.txt > Fl_123_4_lex.cone```

to get the starting cone. Then add to the end of the file  ```Fl_123_4_lex.cone``` the lines 

```
{(1,0,2,3,4,7,8,5,6,9,10,11,13,12),
(1,2,3,0,7,8,4,9,5,6,13,10,11,12),
(13,12,11,10,9,8,7,6,5,4,3,2,1,0)}

{(1,1,1,1,-1,1,1,1,1,1,-1,-1,1,1),
(1,1,1,1,1,1,-1,1,-1,-1,1,1,1,1),
(1,1,1,1,1,1,1,1,1,1,1,1,1,1)}
```

(these lines record the symmetry of the ideal.) Finally, run

```
gfan_tropicaltraverse --symmetry --symsigns < Fl_123_4_lex.cone > Fl_123_4_lex.trop
```

At the end of the notebook ```FansOnTFl4.ipynb```, we verify that the presentation of this fan in the paper agrees with the output fron ```gfan```. 
