# Semi_automated_OBIA_processing_with_local_USPO
This repository contains all the jupyter notebooks used for processing Ouagadougou case study for MAUPP project. The methods and results were published in [1].

It can be easily adapted to use i.cutline, allowing thus for more automated solution for the creation of local zones [2].


----

## Segmentation
Using local USPO approach (in used-provided morphological zones).

## Segment stats
Computation and segment statistics and save of them in a postGis database.

## Classification
Performed using R magicell.
A feature selection (VSURF) procedure is implemented. 
The classification is performed using Random Forest (Caret R package).
In this repo, different tests were perfomed (A: optical only; B: optical nDSM; C: SAR only; D: Optical SAR; E: Optical nDSM NDVI - class 'shadow included')

## Postclassification
Computation of neighborhood matrix at the segment level. Importing of neighborhood matrix, segment labels and segment statistics in PostGis database. Computing for each segment the percentage of borders shared with different classes. Reclassification rules according the neighborhing and segment statistics/informations. 

----
[1]Grippa, Tais, Stefanos Georganos, Sabine Vanhuysse, Moritz Lennert, and Eléonore Wolff. 2017. “A Local Segmentation Parameter Optimization Approach for Mapping Heterogeneous Urban Environments Using VHR Imagery.” In Proceedings Volume 10431, Remote Sensing Technologies and Applications in Urban Environments II. IEEE. [https://doi.org/10.1117/12.2278422](https://doi.org/10.1117/12.2278422).

[2]Georganos, Stefanos, Tais Grippa, Moritz Lennert, Sabine Vanhuysse, Brian Johnson, and Eléonore Wolff. 2018. “Scale Matters: Spatially Partitioned Unsupervised Segmentation Parameter Optimization for Large and Heterogeneous Satellite Images.” Remote Sensing 10 (9): 1440. [https://doi.org/10.3390/rs10091440](https://doi.org/10.3390/rs10091440).
