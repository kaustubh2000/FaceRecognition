# Face Recognition
## About
Program to run facial recognition after training on faces known, and then testing on unknown faces to find matches.<br>
>These programs do not work on the side view of faces.
The face_recognition python library is used from [GitHub](https://github.com/ageitgey/face_recognition)

## To run:
First, install the required libraries by running the following command:
```sh
$ pip3 install opencv-python face_recognition numpy pickle-mixin Pillow
```
Then, create directories:
```sh
$ mkdir known_faces unknown_faces processed
```
Create folders with the name of the person's identity, under the known_faces folder. Insert test images under unknown_faces.<br>
The output of the tested images can be found in the processed directory.

## Optimization:
The optimized version of this code has runs faster. I have used ```Pillow``` to optimize the code slightly and ```pickle``` for dumping trained data into data files.<br>
To train based on images in the subfolders of known_faces:
```sh
$ python3 training.py
```
To test on unknown images placed in the unknown_faces directory:
```sh
$ python3 test.py
```
To see the output, open the folder named "processed" and open images from there. They will be smaller, optimized images but the program runs faster. And the output is pretty accurate.
