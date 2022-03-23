# Writeup: Track 3D-Objects Over Time

Please use this starter template to answer the following questions:

### 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

In the four parts of this project, I had the opportunity to:
1- Visulaize the range image
2- Visualize the gernated point cloud
3- Transform the point cloud to BEV image
4- Perform itensity and height images from the BEV
5- Integrated the fpn_resnet and enable all configs to allow it to work
6- Extract bounding boxes
7- Caluclate iou precision and recall
8- Visulaize results.

For me, the ost difficult part was always the transforamtion of spaces. I fing it not so clear, that I had to research alot to solve the issues and mentors were really helpful.


### 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)? 

For me, camera-lidar fusion allow the possibility to have more than one view over our data, also fills the gap
by creating redundant measurements to minimize errors and guarantee obervations using 2 sensors.

Camera and lidar each has its own benefit, that why using both of them simultaniously provides better results

### 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?
Accuracy.
If we are going to be totally dependent on sensors completely in the future without the driver has to pay an attention, qulaity or perceptions and senor fusion has to guaranteed 100%.

### 4. Can you think of ways to improve your tracking results in the future?
Ensure out trained model capabilities and how to detect to try get the best out of it.
Plausability checks to guarantee sensors performance.

NOTE:
I added couple of pictures showing different views of vehicles according to perceptions and angle.

## Attachement of results according to project instructions
# Project instructions Step 1

# Range Image Result
![2022-03-23_18h49_17](https://user-images.githubusercontent.com/73642186/159763811-8b061a3e-c822-441b-955d-cafcd0bab00f.png)
# PCL Image Result
![2022-03-23_18h52_54](https://user-images.githubusercontent.com/73642186/159764531-337c316b-7672-4ac3-856f-a203553db843.png)

# Examples of vehicles with different views and intensity
![a](https://user-images.githubusercontent.com/73642186/159764683-20d286ed-7b65-4b46-b7a7-72b6e08778b1.PNG)
![b](https://user-images.githubusercontent.com/73642186/159764687-ad92cfbb-ea86-454b-be1b-b25ce93184cd.PNG)
![c](https://user-images.githubusercontent.com/73642186/159764690-3d610dd9-8b33-4538-b118-00673bf3c6da.PNG)
![d](https://user-images.githubusercontent.com/73642186/159764694-cb6edd2e-c813-40c1-999b-d666c43eebb3.PNG)
![e](https://user-images.githubusercontent.com/73642186/159764697-b309903f-6a40-452b-9792-548f98d1f5e8.PNG)


Project instructions Step 2

# BEV Image result
![2022-03-23_19h04_53](https://user-images.githubusercontent.com/73642186/159766487-95af1f6c-87e0-42c6-bded-dc20a46a681b.png)

# Intensity Image Result
![2022-03-23_19h07_50](https://user-images.githubusercontent.com/73642186/159766967-fc8a14c9-f5d6-4200-af1c-a48d58f078c8.png)

# Intensity Image Zoomed Result
![2022-03-23_19h09_10](https://user-images.githubusercontent.com/73642186/159767156-cdc6593e-f6f0-4dc7-b94f-f345155862f9.png)

# Height Image Result
![2022-03-23_19h10_11](https://user-images.githubusercontent.com/73642186/159767333-9c13f7ae-e11b-4879-b64e-a6eaaf9aee1d.png)

# Height Image Zoomed Result
![2022-03-23_19h10_44](https://user-images.githubusercontent.com/73642186/159767410-107c306d-63ef-4331-8f44-3522dd38a887.png)

# Project Intructions Step 3
# Vehicle Detection results
![2022-03-23_19h18_55](https://user-images.githubusercontent.com/73642186/159769575-d13ee299-2243-42b7-9527-76239a930233.png)

As I noted, the model has detected only two vehicles out of 3.


# Project Intructions Step 4

# Precision and recall
configs_det.use_labels_as_objects = False

![2022-03-23_19h38_39](https://user-images.githubusercontent.com/73642186/159772279-abab9f75-bef9-487b-812b-957c50bb276b.png)

precision = 0.9644128113879004, recall = 0.8856209150326797

# Precision and recall

configs_det.use_labels_as_objects = True

![2022-03-23_19h42_41](https://user-images.githubusercontent.com/73642186/159773028-228c760a-d0a9-463a-bdd4-004be33349b8.png)

precision = 1.0, recall = 1.0
