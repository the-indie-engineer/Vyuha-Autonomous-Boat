<h3>Propulsion System</h3>
 The system guarantees the continual output of ASV
power and is an important part of the ASV. It consists of two
direct-current (DC) brushless thrusters powered by a 16 V
lithium-ion battery. The thrusters are equipped with two threeblade propellers with a diameter of 0.076 m, which are adjusted
by two rotary speed controllers, respectively. The ASV contains
a differential steering system and requires two inputs, n1 and n2
to regulate its heading direction, where n1 and n2 are the 2
propeller speeds in Revolutions Per Second (RPS). Electronic
speed control controls the ASV velocity, and the differential
speed controls the steering of the ASV.

<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230269559-92f8111d-4187-4555-8976-cc3ac7fcec79.png">
  <p>Figure 1: Propulsion Control</p>
</div>

Obviously, line motion requires port and starboard thrusters to run
at the identical speed, and the differential thrust is zero during this
case. nc and nd represent the common mode and differential mode
propeller speeds, respectively.

<div align="center">
  <p>𝑛 = (n1 + n2)/2</p>
  <p>n<sub>d</sub> = (𝑛1 − 𝑛2)</p>
</div>

The ASV with the rudderless double thrusters must generate
momentum by the differential thrust between the port and
starboard propellers to vary the heading. During this process, the
velocity of the ASV also changes. So, there's a coupling between
the velocity and the yaw rate. In order to eliminate the results of
coupling and maintain the rate of the ASV, OeXeYe must remain
constant in any respect times, and O<sub>e</sub>X<sub>e</sub>Y<sub>e</sub> changes around zero
reckoning on the direction of the manoeuvre.
The ASV with the rudderless double thrusters must generate momentum by the differential thrust between the port and starboard propellers to vary the heading. During this process, the velocity of the ASV also changes. So, there's a coupling between the velocity and the yaw rate. In order to eliminate the results of coupling and maintain the rate of the ASV, OeXeYe must remain constant in any respect times, and OeXeYe changes around zero reckoning on the direction of the manoeuvre.
<h3>Three-DOF Dynamic Model</h3>
The availability of a sufficiently accurate ASV model enabling effective control design is imperative for both control methodology design and simulation study purposes. This requires a prior investigation of both a precise mathematical ASV model with reasonable system parameters. Generally, the study of a standard ASV dynamic model can be divided into two parts: kinematics, which treats only geometrical aspects of motion, and kinetics, which is the analysis of the forces causing the motion.
<h3>Fail safe mechanism:</h3>
In order to stop the motion of the boat during malfunctioning of the system, we use a kill switch to control its movement. In a fail-safe mechanism, we use transmitter-controlled regulation and Manual switch-based regulation to control the motor in case of fault. By interfacing the Arduino withthe receiver, we get a continuous signal. The receiver and the manual switch are connected to the OR gate. The output of the
OR gate will control the relay. The relay passes the signal to the motor control. The motor will turn ON and OFF according to the signal received from the receiver and the manual switch.

<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230325977-01f8b5ec-6b63-4eec-9474-9cc1cd130cf6.png">
  <p>Figure 2: Fail safe mechanism</p>
</div>


