# Ouaga_full_localapproach
This repository contains all the jupyter notebooks used for processing Ouagadougou case study.

----

## Segmentation
Using local USPO approach (in used-provided morphological zones).
## Segment stats
Computation and segment statistics and save of them in a postGis database.
## Classification
Performed using R magicell.

A feature selection (VSURF) procedure is implemented. 

The classification is performed using Random Forest (Caret R package).

Different tests:
> A : optical only

> B : optical nDSM

> C : SAR only

> D : Optical SAR

> E : Optical nDSM NDVI (class 'shadow included')
## Postclassification
Computation of neighborhood matrix at the segment level. Importing of neighborhood matrix, segment labels and segment statistics in PostGis database. Computing for each segment the percentage of borders shared with different classes. Reclassification rules according the neighborhing and segment statistics/informations. 