<h3>Sensor Units:</h3>

This team proposes the Pixhawk 2.4.8 autopilot with
the rover configuration to control our boat. The boat has two
sensor units to maximize the navigation development. Internal
sensor units are built inside the boat controller and External
sensor units are connected externally to the boat controller.
Internal sensor unit consists sensors like Magnetometer,
Accelerometer and Gyroscope. External sensor unit consists
sensor like Global positioning system (GPS).

![image](https://user-images.githubusercontent.com/109530150/230266026-21f2f7e5-1972-4f6a-a54d-b174bbb2fb7a.png)

<p style="text-align: center;">Sensor Unit Overview</p>

<h2>Internal Sensor Unit (ISU)</h2>

Magnetometer is built and integrated into the main
controller Pixhawk 2.4.8. By sensing the Earth’s magnetic Field,
this sensor will update information on the heading of the boat.
Accelerometer will sense and measure the
acceleration forces acting on the boat to determine boat’s position
in space and monitor the boat’s movement. By combining these
sensors, a good navigation solution will be achieved to track the
desired waypoint for the boat.

<h2>External Sensor Unit (ISU)</h2>

Global Positioning System (GPS) used in this boat
will allow the boat to acquire its latitude and longitude point in
real-time.

<h3>ASV Controller:</h3>
  
ASV controller is a core of our software design. The
Extended Kalman Filter (EKF) is used to estimate boat’s position,velocity, and angular orientation. By combining and fusing the
data from ISU and ESU, EKF will produce the navigation
solution on the boat. Data from the EKF will also be provided to
L1 Control, which is the most powerful function for updating
lateral acceleration on this vehicle. The lateral acceleration will
be crucial for the PID controller in steering adjustment. So, that
the boat may stay on the water at all times on the preferred path.

![image](https://user-images.githubusercontent.com/109530150/230266190-99f73034-3a85-4ebe-ba99-766232fe0108.png)
  <center>Figure 2: Controller overview</center>
  
<h2>Position and Attitude control:</h2>

On the Block of Position and Attitude Control. The
steering output for the ESC Motor will be determined by the L1
Control and PID Controller. With L1 Control, the AHRS and
Waypoint computed from the EKF will be utilized to update the
waypoint and provide the necessary acceleration.
