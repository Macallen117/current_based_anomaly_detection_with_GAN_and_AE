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
<img src="figures/linear_feed_axis_Horizontal_normal_condition_data_with_horizontal_force_changes.jpg" width="450"/>

<img src="figures/linear_feed_axis_horizontal_misalignment_data.jpg" width="450"/>

## CNC data

<img src="figures/CNC_Horizontal normal_condition_data_with_horizontal_force_changes.jpg" width="450"/>

<img src="figures/CNC_Horizontal_normal_condition_data_with_vertical_force_changes.jpg" width="450"/>

<img src="figures/CNC_horizontal_misalignment_data.jpg" width="450"/>

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
<img src="figures/cnn-ae.jpg" width="450"/>

## TCN-AE

<img src="figures/tcn-ae.jpg" width="450"/>

## LSTM-AE

<img src="figures/lstm-ae.jpg" width="450"/>

## CNN-LSTM-AE

<img src="figures/cnn-lstm-ae.jpg" width="450"/>

**Result:**
train on linear feed axis data:

![image](figures/linear_feed_axis_reconstruction_example.jpg)

<img src="figures/linear_feed_axis_loss_distribution_example.jpg" width="450"/>

<img src="figures/linear_feed_axis_classification_example.jpg" width="450"/>

transfer to CNC data

![image](figures/CNC_reconstruction_example2.jpg)

<img src="figures/CNC_loss_distribution_example2.jpg" width="450"/>

<img src="figures/CNC_classification_example2.jpg" width="450"/>

## Related Publication
This project is accompanied by the following published article:

(https://link.springer.com/article/10.1007/s00170-023-12060-2)

Demetgul, M., Zheng, Q., Tansel, I. N., & Fleischer, J. (2023). Monitoring the misalignment of machine tools with autoencoders after they are trained with transfer learning data. The International Journal of Advanced Manufacturing Technology, 128(7), 3357-3373.

##Contributors

Dr.Mustafa Demetgül – Academic Supervisor

Macallen117– Developer
