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
reckoning on the direction of the manoeuvre
