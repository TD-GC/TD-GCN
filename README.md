# TD-GCN

# Prerequisites

```pip install -r requirements.txt```  <br />

```pip install -e torchlight```  <br />

# Data Preparation
**Download NTU RGB+D 60 dataset :** https://rose1.ntu.edu.sg/dataset/actionRecognition <br />
Extract above files to:  ```./data/nturgbd_raw``` <br />
**Download NW-UCLA dataset :** https://www.dropbox.com/s/10pcm4pksjy6mkq/all_sqe.zip?dl=0 <br />
Move  **all_sqe** to:  ```./data/NW-UCLA``` <br />

## Data processing
 ```cd ./data/ntu```
 **#First**
 ```python get_raw_skes_data.py```
 **#Second**
 ```python get_raw_denoised_data.py```
 **#Third**
 ```python seq_transformation.py```
  
