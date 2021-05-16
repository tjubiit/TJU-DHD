## TJU-DHD dataset (object detection and pedestrian detection)

This is the official website for "*[TJU-DHD: A Diverse High-Resolution Dataset for Object Detection (TIP2020)](https://arxiv.org/abs/2011.09170.pdf)*", which is a newly built high-resolution dataset for object detection and pedestrian detection.
- 115k+ images and 700k+ instances
- Scenes: **traffic** and **campus**, Tasks: **object detection** and **pedestrian detection**
- **High resolution**: image resolution of at least 1624x1200 pixels, the object height from 11 pixels to 4152 pixels.
- **Diversity**: A large variance in appearance, scale, illumination, season, and weather
- **Cross-scene evaluation** and **same-scene evaluation**  on pedestrian detection
- If you are interested in pedestrian detection, please refer to [our IEEE T-PAMI paper](https://arxiv.org/pdf/2010.00456.pdf) or [our github project](https://github.com/JialeCao001/PedSurvey).

![Examples of DHD](imgs/diversity.jpg)


## Table of Contents
1. [Introduction](#1)  
2. [Object detection dataset](#2)  
   2.1 [TJU-DHD-traffic](#2.1)  
   2.2 [TJU-DHD-campus](#2.2)   
3. [Pedestrian detection dataset](#3)  
   3.1 [TJU-Ped-traffic](#3.1)  
   3.2 [TJU-Ped-campus](#3.2)   
4. [Benchmark](#4)  
   4.1 [TJU-DHD-traffic](#4.1)  
   4.2 [TJU-DHD-campus](#4.2)   
   4.3 [TJU-DHD-pedestrian](#4.3) 
5. [Citation](#5)  
6. [Evaluation on the test set](#6) 
7. [Contact](#7) 

## 1. Introduction <a name="1"></a>

Vehicles, pedestrians, and riders are the most important and interesting objects in the perception modules of self-driving vehicles and video surveillance. However, the state-of-the-art performance of detecting such important objects (esp. small objects) is far from satisfying the demand of the practical systems. Large-scale, rich-diversity, and high-resolution vehicle and pedestrian datasets play an important role in developing better object detection methods to satisfy the demand. Existing public large-scale datasets such as MS COCO collected from websites do not focus on these specific scenarios. Moreover, the popular datasets (e.g., KITTI and Citypersons) collected from these specific scenarios are limited in the number of images and instances, the resolution, and the diversity in seasons, weathers, and illuminations. To attempt to solve the problem, in this paper, we build a diverse high-resolution dataset (called TJU-DHD). The dataset contains 115,354 high-resolution images (52% images have a resolution of 1624x1200 pixels and 48% images have a resolution of at least 2,560x1,440 pixels) and 709,330 labeled objects in total with a large variance in scale and appearance. Meanwhile, the dataset has a rich diversity in season variance, illumination variance, and weather variance. Based on this object dataset, a new diverse pedestrian dataset is further built. With the four different detectors (i.e., the one-stage RetinaNet, anchor-free FCOS, two-stage FPN, and Cascade R-CNN), experiments about object detection and pedestrian detection are conducted. We hope that the newly built dataset can help promote the research on object detection and pedestrian detection in these two scenes.
## 2. Object detection dataset <a name="2"></a>

| name       | DHD-traffic (\#images) | DHD-traffic (\#instances) | DHD-campus (\#images) | DHD-campus (\#instances) |
| :--------- | :--------------------: | :-----------------------: | :-------------------: | :----------------------: |
| training   |         45,266         |          239,980          |        39,727         |         267,445          |
| validation |         5,000          |          30,679           |         5,204         |          41,620          |
| test       |         10,000         |          60,963           |        10,157         |          68,643          |
| total      |         60,266         |          331,622          |        55,088         |         377,708          |

#### 2.1 TJU-DHD-traffic <a name="2.1"></a>
* training & validation set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/ERPTtJ9Qf3hHnKn9JQc9_y0B5uaq6qXjnF4U--2wiSTjRw?e=aarX3v)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1eLxfl19LVLy9k-DrqTOYvg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_trainval_images.zip)
    * annotations:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EY0m5aX84EJFnquyCE8KSp8BiZKTlNHySbdJ0QG-nE2XTQ?e=Abpvgz)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1xFhMwQgpqk1QILwXS_dR2g)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_trainval_annos.zip)
* test set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EbkVOGVzsoRIhR6u73iAv44BN3n9geqp3R-eTJeZCJen-w?e=az00He)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1b1iR8eujY28qm-pH8rHV-A)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_test_images.zip)
    * imageinfo:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EfuzQvR7qrhAi8oDMy5PheUBvxSL539oua1kD6g130DChg?e=yOhBGM)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1Np079urN0uQmybBM4RriZA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_test_imageinfo.zip)
* evaluation tools:
  [cocoapi](https://github.com/cocodataset/cocoapi)

#### 2.2 TJU-DHD-campus <a name="2.2"></a>
(The training imageset is too large, thus is ziped as a 4-part archive.
One should download all of them and open the `.zip.001` using your favorite zip file extractor.)
* training & validation set:
    * training images-1:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EQOf_tTaDz9AtGBA7xXZdMYBmGgEN3wI6pYxdj_sqU9RaA?e=IAa4z4)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1aar9GAbityEBMMEnXEwbOA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.001)
    * training images-2:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EYdb15b5s3hOm_2EWc_uLn8BtpzXnpZJLVRIH6HdbXfbVw?e=hHJNon)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1xWDiok5DTVT8HEMK09DPiA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.002)
    * training images-3:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EatVjZJ4uJZGm3OOvdbjheMB6dIOlDumkbhVSMqNZFjSDQ?e=5a9C63)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1gUQs6XdUU7fczaydtLPBSg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.003)
    * training images-4:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/ERJGIKSOjrVGodjyAtYWOBIBz7Yn3EGGjmtMRDpG9eFlHQ?e=x8MASb)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1PncIpCpS_En9Ka0aD6-_lA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.004)
    * validation images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EUHmv-SilRtPlKVuV7TTYlUB24CVeAi9HPto9ZJ6m61kpA?e=aREmy0)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1WgbIEXIbGHjh6jBjh_l37A)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_val_images.zip)
    * annotations:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EfJ_SbAK2itJk8kyLBF9ER8BqO0faVumeWn8rPYMkGpqNw?e=Ckc2jn)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1JKnGky_Qzk3QluURgFxCBQ)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_trainval_annos.zip)
* test set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EZZe-4Atw8tEkPdTToNXEboBtdORbKqz2j6asah_hgUgAA?e=ABQibv)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1I33BMKvU9WP_nC64wM1hHw)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_test_images.zip)
    * imageinfo:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EQJpKUI5UUxBuM6ZQGLCLNwBEfGX0tgBR_JyZhAyRp4YYw?e=f6Zrxz)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1LmJRobdmYoqWv1NAqwKcsg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_test_imageinfo.zip)
* evaluation tools:
  [cocoapi](https://github.com/cocodataset/cocoapi)


## 3. Pedestrian detection dataset<a name="3"></a>

| name       | Ped-traffic (\#images) | Ped-traffic (\#instances) | Ped-campus (\#images) | Ped-campus (\#instances) |
| :--------- | :--------------------: | :-----------------------: | :-------------------: | :----------------------: |
| training   |         13,858         |          27,650           |        39,727         |         234,455          |
| validation |         2,136          |           5,244           |         5,204         |          36,161          |
| test       |         4,344          |          10,724           |        10,157         |          59,007          |
| total      |         20,338         |          43,618           |        55,088         |         329,623          |

#### 3.1 TJU-Ped-traffic <a name="3.1"></a>
(Note that the images are same as those in the TJU-DHD-traffic)
* training & validation set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/ERPTtJ9Qf3hHnKn9JQc9_y0B5uaq6qXjnF4U--2wiSTjRw?e=aarX3v)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1eLxfl19LVLy9k-DrqTOYvg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_trainval_images.zip)
    * annotations:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EZ35hrbp2PlBkim37i9BnecBKPTpYE92WjCD3GCnTDIXHA)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1wUdgtibmj16aKXvn57Cnfg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_pedestrian_traffic_trainval_annos.zip)
* test set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EbkVOGVzsoRIhR6u73iAv44BN3n9geqp3R-eTJeZCJen-w?e=az00He)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1b1iR8eujY28qm-pH8rHV-A)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_traffic_test_images.zip)
    * imageinfo:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EaqndNLmmcNOsgoHChviMiIB0eedPO6sgdZJBGPjURq2_Q?e=MEZNyD)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/14KaBUhWWio-KYf_1usMfhw)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_pedestrian_traffic_test_imageinfo.zip)
* evaluation tools:
  [Citypersons API](https://bitbucket.org/shanshanzhang/citypersons)

#### 3.2 TJU-Ped-campus <a name="3.2"></a>
(Note that the images are same as those in the TJU-DHD-campus)
* training & validation set:
    * training images-1:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EQOf_tTaDz9AtGBA7xXZdMYBmGgEN3wI6pYxdj_sqU9RaA?e=IAa4z4)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1aar9GAbityEBMMEnXEwbOA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.001)
    * training images-2:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EYdb15b5s3hOm_2EWc_uLn8BtpzXnpZJLVRIH6HdbXfbVw?e=hHJNon)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1xWDiok5DTVT8HEMK09DPiA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.002)
    * training images-3:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EatVjZJ4uJZGm3OOvdbjheMB6dIOlDumkbhVSMqNZFjSDQ?e=5a9C63)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1gUQs6XdUU7fczaydtLPBSg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.003)
    * training images-4:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/ERJGIKSOjrVGodjyAtYWOBIBz7Yn3EGGjmtMRDpG9eFlHQ?e=x8MASb)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1PncIpCpS_En9Ka0aD6-_lA)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_train_images.zip.004)
    * validation images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EUHmv-SilRtPlKVuV7TTYlUB24CVeAi9HPto9ZJ6m61kpA?e=aREmy0)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1WgbIEXIbGHjh6jBjh_l37A)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_val_images.zip)
    * annotations:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EfyEXYoJ41BErzFfILHIG9YByAgkl2eFd5qHyVrSuPK9AA?e=s5aalT)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/124YE4YjwfkB134NILNa-Dg)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_pedestrian_campus_trainval_annos.zip)
* test set:
    * images:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EZZe-4Atw8tEkPdTToNXEboBtdORbKqz2j6asah_hgUgAA?e=ABQibv)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1I33BMKvU9WP_nC64wM1hHw)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_campus_test_images.zip)
    * imageinfo:
      [OneDrive](https://tjueducn-my.sharepoint.com/:u:/g/personal/hqsun_tju_edu_cn/EXaIKrEGScJNulDTzu9NG8kBk18S03yvfKlNR-bS9NPh1g?e=aUUFBJ)
      / [BaiduNetDisk (code: biit)](https://pan.baidu.com/s/1zNyzTBCVgPZsWW1SbsmNKw)
      / [backup](http://vi.tju.edu.cn/public/dhd_dataset/dhd_pedestrian_campus_test_imageinfo.zip)
* evaluation tools:
  [Citypersons API](https://bitbucket.org/shanshanzhang/citypersons)



## 4. Benchmark <a name="4"></a>

#### 4.1 TJU-DHD-traffic <a name="4.1"></a>

* Results on validation

  | method       | backbone | input size |  AP   | AP@0.5 | AP@0.75 | AP_s  | AP_m  | AP_l  |
  | :----------- | :------: | :--------: | :---: | :----: | :-----: | :---: | :---: | :---: |
  | RetinaNet    | ResNet50 |  1333x800  | 53.5  |  80.9  |  60.0   | 24.0  | 50.5  | 68.0  |
  | FCOS         | ResNet50 |  1333x800  | 53.8  |  80.0  |  60.1   | 24.6  | 50.6  | 68.8  |
  | FPN          | ResNet50 |  1333x800  | 55.4  |  83.4  |  63.0   | 30.4  | 52.2  | 68.2  |
  | Cascade RCNN | ResNet50 |  1333x800  | 57.9  |  82.7  |  66.6   | 32.6  | 54.4  | 71.4  |

#### 4.2 TJU-DHD-campus <a name="4.2"></a>

* Results on validation

  | method       | backbone | input size |  AP   | AP@0.5 | AP@0.75 | AP_t  | AP_s  | AP_l  | AP_l  |
  | :----------- | :------: | :--------: | :---: | :----: | :-----: | :---: | :---: | :---: | :---: |
  | RetinaNet    | ResNet50 |  1333x800  | 48.4  |  79.3  |  52.4   |  4.7  | 27.3  | 56.2  | 73.8  |
  | FCOS         | ResNet50 |  1333x800  | 49.3  |  73.8  |  53.8   |  5.6  | 29.6  | 55.9  | 74.3  |
  | FPN          | ResNet50 |  1333x800  | 52.4  |  77.5  |  58.4   |  8.5  | 37.4  | 58.6  | 74.9  |
  | Cascade RCNN | ResNet50 |  1333x800  | 55.1  |  77.6  |  60.9   | 10.8  | 40.1  | 61.2  | 78.8  |

#### 4.3 TJU-DHD-pedestrian <a name="4.3"></a>

* Miss rate with same-scene evaluation

  | method |  R/RS/HO/R+HO/A (TJU-Ped-campus)  | R/RS/HO/R+HO/A (TJU-Ped-traffic)  |
  | :----- | :---------------------------: | :---------------------------: |
  | FPN    | 27.92/73.14/67.52/35.67/38.08 | 22.30/35.19/60.30/26.71/37.78 |

* Miss rate with cross-scene evaluation

  | method | R/R+HO (TJU-Ped-campus -> traffic) | R/R+HO (TJU-Ped-traffic -> campus) |
  | :----- | :-----------------------------------------: | :---------------------------------------------: |
  | FPN    |              30.62 / 33.89               |               42.08 / 50.55               |

## 5. Citation <a name="5"></a>

If this project help your research, please consider to cite our paper.
```
@article{Pang_DHD_TIP_2020,
         author = {Yanwei Pang and Jiale Cao and Yazhao Li and Jin Xie and Hanqing Sun and Jinfeng Gong},
         title = {TJU-DHD: A Diverse High-Resolution Dataset for Object Detection},
         journal = {IEEE Transactions on Image Processing},
         year = 2020
        }

@article{Cao_PDR_arXiv_2020,
         author = {Jiale Cao and Yanwei Pang and Jin Xie and Fahad Shahbaz Khan and Ling Shao},
         title = {From Handcrafted to Deep Features for Pedestrian Detection: A Survey},
         journal = {arXiv:2010.00456},
         year = 2020
        }
```

## 6. Evaluation on the test set <a name="6"></a>

Ablation studies can be conducted on the validation set.
If you would like to evaluate your model on the test set, you can send us (connor#tju.edu.cn, replace `#` with `@`) your detection results in the `json` format.

## 7. Contact <a name="7"></a>

If you have any questions or want to add your results, please feel free to [contact us](https://github.com/vilabtju/dhd-dataset/issues).
