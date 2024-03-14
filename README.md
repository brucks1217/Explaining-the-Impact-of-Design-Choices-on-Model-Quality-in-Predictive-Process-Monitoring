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
![framework7](https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/9b98382b-d053-4bc7-a241-8afc4341126a)<div align="center">Framework Overview</div>
<br/>

## Next Event Prediction

For phase 1, the hyperparemeter search space is currently defined as :

<div align="center"><img width="739" alt="nextact_ph1" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/42c97582-2b76-4a3b-8b3e-6a40c6d0d1ce"  ></div>
  <div align="center">Hyperparameter values specification in the next activity prediction instantiation of the proposed framework</div>

<br/>
<br/>

<img width="1404" alt="nextact_inst" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/33e05de4-8c1e-460c-ab51-ced12ea0170e">
<div align="center">Experiment detail for next-event prediction instantiation</div>
<br/>

For the Ph.2,
run 'SSE_NextAct.ipynb'
``` 
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
 ┣ SSE_NextAct.ipynb
...
```

You can change the target event log by changing the line : ``` eventlog = 'SEPSIS.csv' ```.

Once you generate the code, the result configurations of hyperparameter values will be stored at 
```
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
...
 ┣ config_nextact
   ┣ BPIC11
   ┣ BPIC12
   ┣ BPIC15
   ┣ SEPSIS
...
```
<br/>

For the Ph.3 and 4,
run 'Exp_NextAct.ipynb'
```
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
...
 ┣ config_nextact
...
   ┗ Exp_NextAct.ipynb
...
```


## Outcome Prediction

For phase 1, the hyperparameter search space is currently defined as :
<div align="center"><img width="744" alt="outcome_ph1" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/f0882392-ed0c-412c-8eee-d5cce7cb550d"></div>
  <div align="center">Hyperparameter values specification in the outcome prediction instantiation of the proposed framework</div>
  
<br/>
<br/>

<img width="1413" alt="outcome_inst" src="https://github.com/brucks1217/Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring/assets/112471517/abeab33c-212a-4f33-a936-5d260aa71707">
<div align="center">Experiment detail for outcome prediction instantiation</div>
<br/>

For the Ph.2,
run 'SSE_Outcome.ipynb'
```
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
...
 ┣ SSE_Outcome.ipynb
...
```

You can change the target event log by changing the line : ``` eventlog = 'SEPSIS.csv' ```.

Once you generate the code, the result configurations of hyperparameter values will be stored at 

```
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
...
 ┣ config_outcome
   ┣ BPIC11
   ┣ BPIC12
   ┣ BPIC15
   ┣ SEPSIS
...
```

<br/>
For the Ph.3 and 4,
run 'Exp_Outcome.ipynb'

```
Explaining-the-Impact-of-Design-Choices-on-Model-Quality-in-Predictive-Process-Monitoring
...
 ┣ config_nextact
...
   ┗ Exp_Outcome.ipynb
...
```

