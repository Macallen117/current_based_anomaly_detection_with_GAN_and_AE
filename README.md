# current_based_anomaly_detection_with_GAN_and_AE

# 1. Requirements
   - pytorch
   - numpy
   - pandas
   - sklearn
   - optuna

# 2. Overview
   - Description: This project is about error detection of linear feed axis and CNC machining center based on motor current data.
   - Flowchart:
   ![image](figures/flowchart.jpg)
   - Procedure:

1. Linear feed axis data pre-training autoencoder
2. Data Augmentation via W-DCGAN
3. Classification of CNC signals via transfer learning

# 3. data collection and preprocessing
## linear feed axis data
![image](figures/linear_feed_axis_Horizontal_normal_condition_data_with_horizontal_force_changes.jpg)
![image](figures/linear_feed_axis_horizontal_misalignment_data.jpg)
## CNC data
![image](figures/CNC_Horizontal normal_condition_data_with_horizontal_force_changes.jpg)
![image](figures/CNC_Horizontal_normal_condition_data_with_vertical_force_changes.jpg)
![image](figures/CNC_horizontal_misalignment_data.jpg)

# 4. data generation using W-DCGAN
![image](figures/GAN.jpg)

## linear feed axis data

![image](figures/linear_feed_axis_movie.gif)
![image](figures/linear_feed_axis_generation_example.jpg)
![image](figures/linear_feed_axis_similarity_check1.jpg)
![image](figures/linear_feed_axis_similarity_check2.jpg)

## CNC data

![image](figures/cnc_movie.gif)
![image](figures/CNC_generation_example.jpg)
![image](figures/CNC_similarity_check1.jpg)
![image](figures/CNC_similarity_check2.jpg)

# 5. Fault detection using various autoencoders
## CNN-AE
![image](figures/cnn-ae.jpg)
## TCN-AE
![image](figures/tcn-ae.jpg)
## LSTM-AE
![image](figures/lstm-ae.jpg)
## CNN-LSTM-AE
![image](figures/cnn-lstm-ae.jpg)

**Result:**
train on linear feed axis data:
![image](figures/linear_feed_axis_reconstruction_example.jpg)
![image](figures/linear_feed_axis_loss_distribution_example.jpg)
![image](figures/linear_feed_axis_classification_example.jpg)
transfer to CNC data
![image](figures/CNC_reconstruction_example2.jpg)
![image](figures/CNC_loss_distribution_example2.jpg)
![image](figures/CNC_classification_example2.jpg)
