# Explaining the Impact of Design Choices on Model Quality in Predictive Process Monitoring

SSE_NextAct.ipynb (Search Space Exploration for Next Activity Prediction) will be uploaded soon

# Datasets
+ BPIC11 : BPIC11_f1 
+ BPIC12 : bpic2012_O_ACCEPTED-COMPLETE
+ BPIC15 : BPIC15_1_f2
+ SEPSIS : sepsis_cases_1

from https://drive.google.com/open?id=154hcH-HGThlcZJW5zBvCJMZvjOQDsnPR 

+ Structure of the repository
``` 
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
 ┣ requirements.txt
 ┣ SSE_NextAct.ipynb
 ┣ SSE_Outcome.ipynb
 ┣ config_nextact
 ┃ ┣ BPIC11
 ┃ ┣ BPIC12
 ┃ ┣ BPIC15
 ┃ ┣ SEPSIS
 ┃ ┗ Exp_NextAct.ipynb
 ┣ config_outcome
 ┃ ┣ BPIC11
 ┃ ┣ BPIC12
 ┃ ┣ BPIC15
 ┃ ┣ SEPSIS
 ┃ ┗ Exp_Outcome.ipynb
 ┣ datasets
 ┗ model_bin
```

# Environment 

+ CPU : Intel i9-12900
+ GPU : Nvidia RTX-3090TI
  
This project is based on the 2.2.0-cuda11.8-cudnn8-runtime Docker image, which includes CUDA 11.8 and cuDNN 8 (Python 3.10.13).

You can download required docker image with :
```
docker pull pytorch/pytorch:2.2.0-cuda11.8-cudnn8-runtime
```
Libraries that are required for the experiment are in the ```requirements.txt```
```
pip install -r requirements.txt
```

# Launching Experiment

## Next Event Prediction
For phase 1, the hyperparemeter search space is currently defined as :

<img width="739" alt="nextact_ph1" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/e951a5d0-e6b3-4593-9abf-28c41382c449">



<img width="1404" alt="nextact_inst" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/33e05de4-8c1e-460c-ab51-ced12ea0170e">
<div align="center">Experiment detail for next-event prediction instantiation</div>

For Ph 2. (Phase 2)
