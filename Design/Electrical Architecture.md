<h2>Electrical Architecture</h2>

The Pixhawk which is an advanced autopilot designer
has a handful of telemetry inputs such as GPS, Buzzer, Receiver,
Hardware safety switch (which operates around 5V) and a power
supply of 14.8v is step down to 5V(the power module provides a
steady 5V to Pixhawk and allows the Pixhawk to measure the
current and voltage of the main battery),Generally these input
signals are given to Pixhawk ,After this process Pixhawk gives
the control signal as output to the servo motors, electronic speed
controller which operates around 8.2V and 14.8V,the servo and
the thruster is connected through an axle shaft, so generally when
the power supply is given the servo motor, the impact of rotation
of the servo motor is transferred through the shaft to the thruster
which results in the movement of the thruster. 

<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230268664-1af1d0fa-8c22-404f-ab10-9785e697d636.png">
    <p>Figure1: Electrical Architecture Overview</p>
</div>

