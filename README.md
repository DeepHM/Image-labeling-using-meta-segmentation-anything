# Image-labeling-using-meta-segmentation-anything
Project of image labeling with the help of meta-segmentation-anything

 <br/> 
 <br/> 
 
## Process overview
1. image load
2. image visualization and point click --> get point

<img src="https://github.com/DeepHM/Image-labeling-using-meta-segmentation-anything/assets/37736774/1016098d-14a3-4f97-bc8d-8edc7ead7700  width="200" height="400"/>

3. Pass the image from 1. and the points from 2. to Segment Anything Model(SAM) to get the image segmentation prediction result
4. Detect outlines using image processing techniques such as findContours and convert them into polygons

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
