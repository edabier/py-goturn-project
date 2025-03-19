#  GOTURN method
### Edgard Dabier, Fabien Senequier & Nolan Sisouphathong

In this project we explore the GOTURN method for object tracking.

### Requirements

In this project we used a pytorch implementation of the GOTURN model made by [amoudgl](https://github.com/amoudgl/pygoturn), so first of all, we need to clone this repository.

To do this, run this the following lines:

`````
cd py-goturn-project
git clone https://github.com/amoudgl/pygoturn.git
`````

You should then follow the tutorial from this repository but here are the main requirements to install:

`````
numpy==1.14.5
torch==1.0.0
opencv-python==4.0.0.21
torchvision==0.2.1
tensorboardX==1.6
````` 

You should also download the weights of the pretrained GOTURN model at this [link](https://drive.google.com/file/d/1szpx3J-hfSrBEi_bze3d0PjSfQwNij7X/view?usp=sharing) and place it in the folder containing the code of the cloned repository.

Once this is done, you should be able to run our code properly.