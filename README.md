# Mutational antigenic profiling of 1-18
### Adam S. Dingens, Jesse Bloom
### In collabortation with Florian Klein's group, particularly Philipp Schommers and Henning Gruell.

We are performing mutational antigenic profiling of 1-18, using the BG505.T332N mutant Env libraries, first described and characterized in [Haddox, Dingens et al 2018](https://elifesciences.org/articles/34420). The triplicate mutant libraries examined here correspond to the three BG505 replicates in this paper. Replicates annotated with an additional letter (i.e. "rep 1b") were done on an indepdent day and have their own mock selected control. 

The _fraction surviving_ statistic used in this analysis is explained in detail [here](https://jbloomlab.github.io/dms_tools2/fracsurvive.html). Our first mutational antigenic profiling analysis of escape from PGT151 using the BF520 env libraries was published [here](http://dx.doi.org/10.1016/j.chom.2017.05.003) in June 2017, and this original analysis is located [in this ipython notebook](https://github.com/adingens/BF520_MutationalAntigenicProfiling_PGT151).

We use [dms_tools2](https://jbloomlab.github.io/dms_tools2/) to analyze these data. This notebook processes the Illumina deep sequencing data software package, and then analyzes the selection in the context of the antibody. Experiments and analysis performed by Adam Dingens in the [Bloom lab](http://research.fhcrc.org/bloom/en.html) in early 2019. 


## Running the analysis
The main analysis is performed by the Jupyter notebook [analysis_notebook.ipynb](analysis_notebook.ipynb).

To run [analysis_notebook.ipynb](analysis_notebook.ipynb) and generate the [Markdown results](results/analysis_notebook.md), run the bash script [run_notebook.bash](run_notebook.bash) with:

./run_notebook.bash

On the Hutch cluster, you probably want to submit this job using [slurm](https://slurm.schedmd.com/), which you can simply do with:

sbatch -p largenode -c 16 --mem=100000 run_notebook.bash


## Organization
The mutational antigenic profiling analysis is performed by the iPython notebook [`analysis_notebook.ipynb`](analysis_notebook.ipynb). 

Subdirectories:

   * `./results/` iss generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb). It contains the `codoncounts` and `differential selection` data and raw output for all figures.
   
   * `./results/FASTQ_files/` contains the input Illumina deep sequencing data. This file is generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb), which downloads the sequencing files from the [Sequence Read Archive](http://www.ncbi.nlm.nih.gov/sra).

   * `./data/` contains all input data needed to run [`analysis_notebook.ipynb`](analysis_notebook.ipynb)). Files are described in the iPython notebok when used. 


## Results and Conclusions
All of the results are breifly detailed in the [`analysis_notebook.ipynb`](analysis_notebook.ipynb) notebook; click on this notebook to see the results.



