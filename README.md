# Green Screening Implementation

This a simple implementation of the green screening process for images implemented in Python and MATLAB. Green Screening / the Green Screen algorithm is often used to change the background behind an _object_ with a background of our choice. This process is widely used in applications where the background needs to be changed.

## About the Green Screening algorithm

The process requires two images as it's input - _foreground_ image and _background_ image. The foreground image must have an object placed over a _green_ background. The background image can be any image of our choice. These images should have the same dimensions. The output we get will have the same dimensions as well.

During the process, a new image (say _output_) is created. The pixels of the output image are taken depending on the following process: the algorithm checks every pixel of the _foreground_ image for the intensity of the green color. If the intensity of the green color is beyond a certain threshold (say 240), then the _output_ image will have the corresponding pixel taken from the _background_ image, else the corresponding pixel is taken from the _foreground_ image. This way the pixels are populated in the _output_ image. This is the working of the green screen algorithm.

## File Description

- [green.m](green.m): Run the process in MATLAB.

- [green.py](green.py): Run the process in Python. Requirements:
  - PIL (pillow) imaging library
  - Numpy

## Requirements

- An image with an object over a green background as shown below: Foreground (_images/fg.png_): <br>
  ![Foreground](images/fg.png) <br>

- A background image (_images/bg.png_): <br>
  ![Background](images/bg.png) <br>

- Make sure both images are of the same dimensions.

## Output achieved

Here is the output achieved with a threshold of 235:

![Output](images/output.png)
