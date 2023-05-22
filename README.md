# Image-labeling-using-meta-segmentation-anything
Project of image labeling with the help of meta-segmentation-anything

 <br/> 
 <br/> 
 
## Getting Started

Create virtual environment:
```
conda create -n {project_name} python=3.8
conda activate {project_name}
pip install jupyter
python -m ipykernel install --user --name {project_name} --display-name "{project_name}"
```

- for meta-segmentation-anything

The (meta-segmentation-anything)code requires python>=3.8, as well as pytorch>=1.7 and torchvision>=0.8. Please follow the instructions [here](https://pytorch.org/get-started/locally/) or [here](https://pytorch.org/get-started/previous-versions/) to install both PyTorch and TorchVision dependencies. Installing both PyTorch and TorchVision with CUDA support is strongly recommended.

Example for local window:
```
pip install torch==1.8.0+cpu torchvision==0.9.0+cpu torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
```

Install Meta Segment Anything:

```
pip install git+https://github.com/facebookresearch/segment-anything.git
```

Install other required packages:
```
pip install jupyter
pip install opencv-python
pip install matplotlib
```
