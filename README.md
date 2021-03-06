# RPR-Loc
Official code for MICCAI2021. ['Contrastive Learning of Relative Position Regression for One-Shot Object Localization in 3D Medical Images'](https://arxiv.org/abs/2012.07043)
![image](https://github.com/LWHYC/RPR-Loc/blob/main/Framework.png)
## Data format
the data format should be like:
```
├── train
│   └── 001
│         └── data.nii.gz
|   └── 002
│         └── data.nii.gz
|   .
|   .
|   .
└── valid
|   └── 00N
|      └── data.nii.gz
|   .
|   .
|   .
└── test
|   └── 00X
|      └── data.nii.gz
|   .
|   .
|   .
```
The name of data division folder should be train/valid/test while the folder name of each volume could be arbitrary.
## Preprocess
The preprocess contains two stage:
1. Resample: use `data_process/Resample_data.py`
2. Normalization: use `data_process/Normalize_data.py`
## Training
Use `train/train_position.py`.  
The config file is in `config`, containing 4 files for coarse/fine & pancreas/head and neck dataset.  
You can choose anyone by changing the `config_file` in line 173 of `train.py`.

