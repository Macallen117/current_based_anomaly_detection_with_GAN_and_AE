# current_based_anomaly_detection_with_GAN_and_AE


# 1. Overview
   - Description: This project is about error detection of linear feed axis and CNC machining center based on motor current data.

# 2. Requirements
   - pytorch
   - numpy
   - pandas
   - sklearn
   - optuna

# 3. data generation using W-DCGAN
![image](images/paper_Images/Pre1.png)

# 4. Fault detection using various autoencoders
## CNN-AE
![image](images/paper_Images/Pre1.png)
![image](images/paper_Images/Pre2.png)

**Procedure:**
1. initiates a seed triangle and scans the surrounding triangles of the seed.  
   the seed is now chosen as the first index of a ordered set to save time.
2. If the angle between the normal of the seed triangle and the normal of a nearby triangle is smaller than the first threshold,
   the adjacent triangle is clustered into the same facet as the seed triangle. 
3. After clustering the first facet, the algorithm initiates a new seed triangle and repeats. 
   the second threshold is not be used to reduce the computational time.
   I currently use a set to contain the index of all the segmented triangles. The new seed is chosen as the first index of the rest unsegmented triangle set.
------

**Result:**

![image](images/seg_Results/seg_Zahnrad.png)
