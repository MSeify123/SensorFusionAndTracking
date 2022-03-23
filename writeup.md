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


###Range Image
