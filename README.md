# Image-labeling-using-meta-segmentation-anything
Image segmentation labeling project with the help of meta-Segment Anything Model(SAM)

## Process overview
1. image load
2. image visualization and point click (using opencv) --> get point(yellow)

![a](https://github.com/DeepHM/Image-labeling-using-meta-segmentation-anything/assets/37736774/1b0c168a-cdfe-4b43-9a26-efd8838ed827)

3. Pass the image from 1. and the points from 2. to SAM to get the image segmentation prediction result

![bb](https://github.com/DeepHM/Image-labeling-using-meta-segmentation-anything/assets/37736774/5a40478c-9102-434a-b3d5-255c8634cf02)

4. Detect outlines using image processing techniques such as findContours and convert them into polygons
5. After creating dictionary according to the file format of labelme "annotation.json" for the polygons in 4., save the new json with the image
6. Read the json created above and the working image (from Labelme)
7. After that, check whether the generated polygon annotation is normal or not, save it as it is if it is perfect, and if there is a slight error, correct some of it and save it.

![ccc](https://github.com/DeepHM/Image-labeling-using-meta-segmentation-anything/assets/37736774/bbe9d3f6-c4ba-4a37-a7c1-bab8da9bb042)

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

Example for local windows:
```
pip install torch==1.8.0+cpu torchvision==0.9.0+cpu torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
```

Install Meta Segment Anything:

```
pip install git+https://github.com/facebookresearch/segment-anything.git
```
Download a model checkpoint:

[here](https://github.com/facebookresearch/segment-anything#model-checkpoints)

- Install other required packages
```
pip install jupyter
pip install opencv-python
pip install matplotlib
pip install labelme
# pip install pycocotools or pip install pycocotools-windows
```
