# Data Analysis for the McMaster Experimental Reduced Gravity Team
The analysis herein was written by Paula Bosca. 

**TO DO**
- Clip data appropraitely so time spent above XX isn't awful and horrible unscientific. 
	- Rerun stats. 

*Backlog*
- Load cells? 
- Acc data??



## Repo Structure 
**Note that since the folder restructing, some of the older notebooks may have data paths that are no longer accurate. Sorry.**

### /Data
`/fc72/` holds data from 2021 Flight campaign which used 3M's FC-72 (TM). 

`/water/` holds data from the 2019 Flight campaign which used water. 

### /IAC_ppr 
This folder contains all the files related to the analysis conducted for the IAC 2021 Presentation and Manuscript. 


`*_stats.ipynb` (* == water of fc72) holds the majority of the work done for the actual IAC presentaiton/paper. 
The water and fc72 notebooks are *basically* the same thing. 
Both have visualisations of the fluid (plotting slices for three diff times as an example of what the data looks like). 
Both have stats on Nab\*\*, Timeto\*\*, Frac\*\* 

`water_stats.ipynb` has manual clipping of parabolas since the data was one big excel of all the parabs. 
Aka, I plotted it and there's clear Max Height ==0 differentiating parabolas.
From the plots, I chose values where the max height was 0 to split the data into the diff parabolas. 


`Combining_parabs.ipynb` Does some of the good df manipulations, adding Nab\*\* (Number of slices above \*\*% of the total chamber height). 
Also creates a summary df with "Time to \*\*" where each cam-parab combo has the time it takes for any single slice to reach \*\* of the total chamber height. 
I think I used this notebok to test stat methods and check some residuals, so there are some boxplots and QQPlots at the bottom. 
This notebook also has my playing around with rolling averages and what those looked like with different "windows" (rolling average of every 10 points, 15, etc)
Has some good loops used for plotting far too many things on one plot, also solid matplotlib fonts. 

`PrelimVis.ipynb` hold the preliminary visualisation done to inspect the FC-72 data.


### /misc
This folder holdks miscellaneous stuff that could be used in the future but is likely just archiveable

`*_loadcell.ipynb` (* == water or fc72) has first visualisations of loadcell data. 

