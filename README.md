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
 ```cd ./data/ntu``` <br />
 **#First** <br />
 ```python get_raw_skes_data.py``` <br />
 **#Second** <br />
 ```python get_raw_denoised_data.py``` <br />
 **#Third** <br />
 ```python seq_transformation.py``` <br />
  
# Training & Testing
## Training <br />
```python main.py --config config/nturgbd-cross-subject/default.yaml --work-dir work_dir/ntu/csub/tdgcn --device 0``` <br />
## Testing <br />
```python main.py --config <work_dir>/config.yaml --work-dir <work_dir> --phase test --save-score True --weights <work_dir>/xxx.pt --device 0``` <br />
