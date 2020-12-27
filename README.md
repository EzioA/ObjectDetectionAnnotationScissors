# Introduction
 
 This tool help you to divide your images and annotations into patches  
 ...when the images are tooooooo <font size=5>big</font>.

 For example, we are going to divide this image into 4 patches:  
 ![panda](https://github.com/EzioA/ObjectDetectionAnnotationScissors/blob/main/assets/panda_gt.png)  
 and the first patch looks like this:  
 ![panda_patch](https://github.com/EzioA/ObjectDetectionAnnotationScissors/blob/main/assets/panda_0_gt.png)


# Usage
```
$ python crop_image_and_objects.py --data_dir dataset --mode voc --h_slice 2 --w slice 2
```
The directory _**dataset**_ contains all the images and corresponding annotations, and the script will create directories recursively as below.  
The directory _**cropped\_images**_ contains all the cropped images for the usage, such as inference. If u need these images, use argument _**crop\_only**_.
```
dataset
├── cropped_images
├── voc
│   ├── images
│   └── labels
└── yolo
    ├── images
    └── labels
```
Now this script supports mode _**voc**_ and _**yolo**_. For more information, use the help docs:
```
$ python crop_image_and_objects.py --help
```

# Update
v0.2 Fix some bugs within VOC annotations, and add the argument _**crop\_only**_.  
v0.1 Raw version.