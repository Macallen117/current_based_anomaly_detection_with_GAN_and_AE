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
![image](figures/linear feed axis Horizontal normal condition data with horizontal force changes.jpg)
![image](figures/linear feed axis horizontal misalignment data.jpg)
## CNC data
![image](figures/CNC_Horizontal normal condition data with horizontal force changes.jpg)
![image](figures/CNC_Horizontal normal condition data with vertical force changes.jpg)
![image](figures/CNC_horizontal misalignment data.jpg)

# 4. data generation using W-DCGAN
![image](figures/GAN.jpg)

## linear feed axis data
linear feed axis movie.gif

![image](figures/linear feed axis generation example.jpg)
![image](figures/linear feed axis similarity check1.jpg)
![image](figures/linear feed axis similarity check2.jpg)

## CNC data
cnc movie.gif

![image](figures/CNC generation example.jpg)
![image](figures/CNC similarity check1.jpg)
![image](figures/CNC similarity check2.jpg)

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
![image](figures/linear feed axis reconstruction example.jpg)
![image](figures/linear feed axis loss distribution example.jpg)
![image](figures/linear feed axis classification example.jpg)
transfer to CNC data
![image](figures/CNC reconstruction example2.jpg)
![image](figures/CNC loss distribution example2.jpg.jpg)
![image](figures/CNC classification example2.jpg)
