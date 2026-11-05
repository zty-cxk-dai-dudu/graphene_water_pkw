# zty model and training-data inventory (historical records)

The records below were checked on zty on 2026-11-05. They identify available historical artifacts; they are not an assertion that these are the final manuscript models.

| Model record | Completed steps | Mounted training geometries | DFT reference / note |
| --- | ---: | ---: | --- |
| 1L model 001 | 200,000 | 1,800 | BLYP-D3 in a nine-frame follow-up validation |
| 2L model 001 initial | 100,000 | 956 | PBE-D3(BJ) |
| 2L model 001 after PIMD labels | 300,000 | 5,966 | PBE-D3(BJ); 5,010 added frames from ten 501-frame CP2K runs |
| 4L model 001 | 500,000 | 42,516 | PBE-D3(BJ) |

The corresponding training and validation arrays are stored on zty in DeePMD format (`type.raw`, `type_map.raw`, and `set.*` directories containing `box.npy`, `coord.npy`, `energy.npy`, and `force.npy`). The 4L training and validation directories alone total approximately 1.40 GB, and each frozen model is approximately 126–149 MB. They are not yet copied into this repository.

An additional 4L ion-pair labeling set contains 590 unique geometries, divided into 528 training and 62 validation frames. A 1L ion-state fine-tuning set contains 160 training and 41 disjoint validation frames. A separate 2L fine-tuning record includes 201 ion-state frames and uses an 80:20 sampling probability for base versus ion-state data.

The historical model training logs report DeePMD-kit 2.1.1. DeePMD-kit 3.1.0 appears in a later inference/validation environment and should not be substituted for the training version.

Required before a definitive model/data upload: identify the exact frozen model for each 1L/2L/4L production and pKw calculation, confirm the matching DFT reference and complete train/validation directories, and regenerate source tables for the final declared analysis windows.
