# Detachable Novel Views Synthesis of Dynamic Scenes Using Distribution-Driven Neural Radiance Fields

We provide one demo scene S5 in /data/URBAN/. And the corresponding pretrained model is in /D4NeRF/logs/S5.

## Setup&Dependency
The code is tested with Python == 3.8.8, Pytorch == 1.11.0 and CUDA == 11.3, the dependencies includes:

* scikit-image
* opencv
* imageio
* cupy
* kornia
* configargparse

## Train
```
python train.py --config configs/config_S5.txt 
```
## Evaluation
```
python evaluation_URBAN.py --config configs/config_S5.txt 
```
## Novel view synthesis
fixed time and view interpolation:
```
python view_render.py --config configs/config_S5.txt --fixed_time --target_idx 15
```

time interpolation and view interpolation:
```
python view_render.py --config configs/config_S5.txt --no_fixed --target_idx 15
```




