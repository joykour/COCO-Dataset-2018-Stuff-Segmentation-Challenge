# COCO Dataset 2018 Stuff Segmentation Challenge

Internship project in Bennett University under Leadinginadi.ai

## Getting Started

Problem Statement :-<br/>
To perform Semantic Segmentation of Stuff classes.The COCO Stuff Segmentation Task is designed to push the state of the art in semantic    segmentation of stuff classes.


### Prerequisites and installing

pip install tensorflow-gpu<br/>
pip install tqdm<br/>
pip install keras<br/>
pip install keras-segmentation<br/>

## Dataset format

You need to make two folders<br/>

Images Folder - For all the training images<br/>
Annotations Folder - For the corresponding ground truth segmentation images<br/>
The filenames of the annotation images should be same as the filenames of the RGB images.<br/>

## Usage via command line 
 
### Visualizing the prepared data

```
python -m keras_segmentation verify_dataset \
 --images_path="dataset1/images_prepped_train/" \
 --segs_path="dataset1/annotations_prepped_train/"  \
 --n_classes=50
```



