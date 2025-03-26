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

The file `test.py` is a modified version of the same file in the original repository. We have added a parameter to be able to conveniently load processed or not processed images to be able to run our tests. This file should be replaced by ours in the pygoturn folder in `pygoturn/src/` in order to work correctly.

To use our implementation of the GOTURN model, we need the video in which we want to track an object to be formated in the `OTB` format. For that, we first need to have a folder containing both the sequence images (in the `.bmp` format) and the corresponding groundtruth segmentation maks for every frame (in the `.png` format). Then, we use the `add-bounding-box.ipynb` notebook which creates a `groundtruth_rect.txt` file for every sequence, containing the groundtruth bounding box coordinates of the tracked object, as well as creating a folder with the name of the sequence, with a subfolder named `img`. The user will then have to rename the `groundtruth_rect.txt` by removing the name of the sequence in the begining of the file name, and place it in the corresponding sequence's folder. Then, all sequences' folders should be placed in a single folder named `sequences`.

Once this is done, you should be able to run our code properly, which is contained in the `Project_test.ipynb` file.

All the code from the beginning, up to the **GOTURN method** section was provided at the beginning of the project as baseline tools to evaluate our method.

Then, inside the **GOTURN method** section, running the `main` method will run the object tracking algorithm on the image sequence defined by `seq` with the parameter `processed` set to True to apply it on processed images, and False otherwise.

Inside this main method is defined the path the pretrained model's wieghts, it has to be changed if it doesn't match your folder's organization.
