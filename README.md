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
```
python -m keras_segmentation visualize_dataset \
 --images_path="dataset1/images_prepped_train/" \
 --segs_path="dataset1/annotations_prepped_train/"  \
 --n_classes=50
 ```
 ### Training the Model
 
 ```
 python -m keras_segmentation train \
 --checkpoints_path="path_to_checkpoints" \
 --train_images="dataset1/images_prepped_train/" \
 --train_annotations="dataset1/annotations_prepped_train/" \
 --val_images="dataset1/images_prepped_test/" \
 --val_annotations="dataset1/annotations_prepped_test/" \
 --n_classes=300 \
 --input_height=320 \
 --input_width=640 \
 --model_name="pspnet"
```
### Getting the predictions
```
python -m keras_segmentation predict \
 --checkpoints_path="path_to_checkpoints" \
 --input_path="dataset1/images_prepped_test/" \
 --output_path="path_to_predictions"
 ```
## References
1. https://github.com/divamgupta/image-segmentation-keras<br/>
2. https://github.com/GeorgeSeif/Semantic-Segmentation-Suite<br/>
3. https://github.com/aurora95/Keras-FCN<br/>
4. http://cocodataset.org/#stuff-2018<br/>
5. https://arxiv.org/abs/1612.03716<br/>

