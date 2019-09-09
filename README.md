# DHD: A Diverse High-Resolution Dataset for Object Detection and Pedestrian Detection

## Introduction

  The new diverse high-resolution dataset (called DHD) is built to focus on object detection in traffic and campus scenes. The dataset contains 115,354 high-resolution images (at least 1624x1200 pixels) and 709,330 labeled objects in total with a large variance in scale and appearance. Meanwhile, the dataset has a rich diversity in season variance, illumination variance, and weather variance. Based on this object dataset, a new diverse pedestrian dataset is further built. We hope that the newly built dataset can help promote the research on object detection and pedestrian detection in these two scenes.

## Datasets

1. object detection in the DHD

   ![Statistics of object detection in the DHD](imgs/dataset-obj.png)
 
    * DHD-traffic: 
        * __training set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __validation set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __test set__: images: [OneDrive]()/[GoogleDrive](); imageinfo: [OneDrive]()/[GoogleDrive]()
        * __evaluation tools__: [cocoapi](https://github.com/cocodataset/cocoapi)
    *	DHD-campus
        * __training set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __validation set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __test set__: images: [OneDrive]()/[GoogleDrive](); imageinfo: [OneDrive]()/[GoogleDrive]()
        * __evaluation tools__: [cocoapi](https://github.com/cocodataset/cocoapi)
    
2. pedestrian detection in the DHD

   ![Statistics of pedestrian detection in the DHD](imgs/dataset-ped.png)
 
    *	Ped-traffic (Note that the images are same as those in the DHD-traffic): 
        * __training set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __validation set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __test set__: images: [OneDrive]()/[GoogleDrive](); imageinfo: [OneDrive]()/[GoogleDrive]()
        * __evaluation tools__: [cocoapi](https://github.com/cocodataset/cocoapi)

    *	Ped-campus (Note that the images are same as those in the DHD-campus):
        * __training set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __validation set__: images: [OneDrive]()/[GoogleDrive](); annotations: [OneDrive]()/[GoogleDrive]()
        * __test set__: images: [OneDrive]()/[GoogleDrive](); imageinfo: [OneDrive]()/[GoogleDrive]()
        * __evaluation tools__: [cocoapi](https://github.com/cocodataset/cocoapi)

## Benchmark

### DHD-traffic

![Result table for DHD-traffic](imgs/benchmark-traffic.png)
 
### DHD-campus

![Result table for DHD-campus](imgs/benchmark-campus.png)
 
### DHD-pededstrian

|     | Ped-campus  | Ped-traffic |
| --- |:-----------:| -----------:|
| FPN | 24.90/34.34 | 29.39/43.22 |
