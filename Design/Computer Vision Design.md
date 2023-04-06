<h2>Computer Vision</h2>
<h3>Software Architecture:</h3>
We have used the Nvidia Jetson Tx2 nano as our on-board computer. This 7.5-watt single board computer on a module brings true AI computing to the edge. It features a variety of standard hardware interfaces that make it easy to integrate it into a wide range of products and form factors. For vision, we have used zed 2i, a stereo camera and LiDAR s2 to detect objects with spatial context and combine AI with 3D localization and consistent ranging resolution. To obtain the best of results, we planned the software architecture by considering these three parameters: Perception, planning and control.
<h3>Perception</h3>
In perception, we focus on integration of sensors and object detection. For object detection we used YOLOv5. It is a family of compound-scaled object detection models trained on the COCO dataset, and includes simple functionality for Test Time Augmentation (TTA), model assembling, hyperparameter evolution, and export to ONNX, CoreML and TFLite. The fusion of light detection and ranging (LiDAR) and camera data in real-time is important to enabling the depth of objects as well as the detection of objects at short and long distances and this has been achieved.
<h3>Planning</h3>
Using the data obtained from the perception sub-system, the vehicle performs behaviour planning wherein the most optimal behaviour to be adopted by the vehicle needs to be decided by predicting states of the vehicle as well as other dynamic objects in the environment into the future by certain prediction horizon Based on the planned behaviour, the motion planning module generates an optimal trajectory, considering the global plan as well as hard and soft motion constraints by working on various algorithms like Voronoi Diagram , Cost Maps , State Lattices and Driving Corridor.
<h3>Control</h3>
The control sub-system is responsible for accurately tracking the trajectory provided by the planning sub-system and for the same, we established the communication with NVidia jetson Tx2 and Pixhawk flight controller using serial communication by pymavlink and mavproxy for sending the commands to Pixhawk flight controller for ai based navigation.
<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230325196-c26f4753-2c52-43df-865a-384e38af223d.png">
  <p>Figure 1: Software architecture</p>
</div>
