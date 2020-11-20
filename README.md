# Capstone_Object_Detection
This repository is the final Capstone Project for Data Science & Artificial Intelligence program

Notes: Tensorflow model on custom data (Transfer Learning).The objective is to identify Formula One Racing Team. Please contact me if you are interested in the inference graph

Instructions: Download and install tensorflow model. The files have been converted to Jupyter Notebook for marking reason. However, i do recommended to use the python files for implementation.

Python code command: 

1. Generate csv from xml:
python xml_to_csv.py

2. Generate TFRecords from csv: \
python generate_tfrecord.py --csv_input=images/train_labels.csv --image_dir=images/train --output_path=train.record \
python generate_tfrecord.py --csv_input=images/test_labels.csv --image_dir=images/test --output_path=test.record \

3. Model training:
python model_main_tf2.py --pipeline_config_path=training/faster_rcnn_resnet101_v1_800x1333_coco17_gpu-8.config --model_dir=training --alsologtostderr

4. Tensorboard: 
python --logdir=training/train

5. Extract inference graph:
python exporter_main_v2.py --pipeline_config_path training/faster_rcnn_resnet101_v1_800x1333_coco17_gpu-8.config --trained_checkpoint_dir training --output_directory inference_graph


