# Urban-Zone-Aerial-Object-Detection
A repository that contains a dataset contains a combination of 3 other datasets. These are the Stanford Drone Dataset (SDD), the Vision Meets Drone (VisDrone) and Unmanned Aerial Vehicles Benchmark Object Detection and Tracking (UAVDT).

This dataset contains 187.138 images and over 4.112.482 annotated objects, the annotation being in the style of YOLOv5.

The dataset is already partitioned into training, testing and validation. The following tables demonstrate how many images and annotations each partition has.

Table I - Dataset images partitions
|Dataset|Train|Test|Validation|
|-------|-----|----|----------|
|SDD|73.092|15.663|15.663|
|VisDrone|29.686|6.301|6.324|
|UAVDT|28.341|5.970|6.098|
|Total|131.119|27.934|28.085|

The dataset has the following objects of interest: person, small vehicle, medium vehicle, large vehicle. The objects are in Portuguese and are respectively pessoa, veículo-pequeno, veículo-médio e veículo-grande.

Table II - Dataset annotations partitions by class

|Class|Train|Test|Validation|Total|
|-----|-----|----|----------|-----|
|Pessoas|1.039.328|225.216|220.918|1.485.462| 
|Veículos-Pequenos|460.431|100.167|98.148|658.746|
|Veículos-Médios|1.287.414|272.524|274.308|1.834.246|
|Veículos-Grandes|94.052|20.091|19.885|134.028|

Using the YOLOv5s object detection and classification model, it was possible to achieve a mAP of 67.2% in this dataset. The table below shows the result of the model performance test.

Table II - Results of a YOLOv5 test
|Class|Images|Labels|P|R|mAP @.5|mAP @.5:.95|
|-----|------|------|-|-|-------|-----------|
|all|27887|750620|0.752|0.628|0.672|0.358|
|pessoa|27887|224458|0.682|0.609|0.626|0.225|
|veiculo-pequeno|27887|99601|0.737|0.65|0.669|0.251|
|veiculo-medio|27887|272464|0.856|0.897|0.916|0.597|
|veiculo-grande|27887|20089|0.843|0.837|0.877|0.612|

The dataset is hosted on Kaggle, by following the link: https://www.kaggle.com/sganderla/urban-zone-aerial-object-detection-dataset

# Acknowledgements

@inproceedings{robicquet2016learning,
title={Learning social etiquette: Human trajectory understanding in crowded scenes},
author={Robicquet, Alexandre and Sadeghian, Amir and Alahi, Alexandre and Savarese, Silvio},
booktitle={European conference on computer vision},
pages={549--565},
year={2016},
organization={Springer}
}

@inproceedings{du2018unmanned,
title={The unmanned aerial vehicle benchmark: Object detection and tracking},
author={Du, Dawei and Qi, Yuankai and Yu, Hongyang and Yang, Yifan and Duan, Kaiwen and Li, Guorong and Zhang, Weigang and Huang, Qingming and Tian, Qi},
booktitle={Proceedings of the European Conference on Computer Vision (ECCV)},
pages={370--386},
year={2018}
}

@article{zhu2020vision,
title={Vision meets drones: Past, present and future},
author={Zhu, Pengfei and Wen, Longyin and Du, Dawei and Bian, Xiao and Hu, Qinghua and Ling, Haibin},
journal={arXiv preprint arXiv:2001.06303},
year={2020}
}
