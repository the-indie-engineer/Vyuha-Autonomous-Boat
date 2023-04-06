<h2>Propulsion System Testing</h2>
The motion control problem for ASVs has been
studied with a focus on those equipped with rudderless double
thrusters due to their simple mechanical structure, flexible
steering capability and some other associated benefits. It
provides guidance for the modeling of general ASVs with
rudderless double thrusters. Then, the model parameters were
identified and verified through some standard motion
measurements, including the acceleration test, circle test and
zigzag test. Finally, based on the dynamic model, the Pixhawk
control was employed to perform the path- following control
of the ASV. Moreover, the controller could maintain good
performance in both line and curve path-following. By
consuming these advantages, we achieved the tasks mentioned
by Roboboat competition.
<h3>System Identification and Experimental Validation</h3>The goal of system identification is to obtain a
simplified understanding of how the vehicle behaves, so that
the control algorithm can accurately calculate control outputs
to produce the desired vehicle response. System identification
that requires a specific set of input time histories, extracts
thrust and hydrodynamic parameters from standard motion
measurements, which include the accelerationtest, circle
test and zigzag test. These tests are all open loop
maneuverability tests. The data can be obtained from these
tests by setting the speeds of the port and starboard
propellers manually.
<h2>Simulink model:</h2>
<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230296049-5088ccfa-0fb3-4d4f-90f1-080cee49c224.png">
  <p>Figure 1: Differential control</p>
</div>
<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230296216-2a2a0489-547e-4067-b924-a28248d2c9ee.png">
  <p>Figure 2: Voltage – Power characteristics of T200</p>
</div>
<h2>Thruster Performance Experiment</h2>
In order to achieve motion control of the ASV, we
need to know the relationship between control signal and the
thrust on the ASV. For this test, the ASV was tied to a tension
meter, connected to a fixed pole. Port and starboard thrusters
were controlled by the same control signals to apply the thrust
uniformly in the surge direction. When the line connecting the
tension meter and the ASV was tight, that is, when the tension
was stable, the tension meter reading could be obtained. The
reading was the total thrust of the propulsion system. Three
experiments were performed under the same experimental
conditions, and the average of three readings of the tension
meter was used as the final experimental result.

The corresponding thrust values under different control
signals.

|PWM Signal(%)| 0 |10 |15 |23 |32 |39 |45| 52 |63 |69| 74 |81| 92| 99|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Thrust (N) |0| 12| 15| 25 |33| 40| 45 |53| 64 |70| 75 |80| 93| 100|

<p align="center">Table 1: PWM signal vs Thrust characteristics</p>

<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230297618-b6f9203b-d050-4bb8-986d-5b810f14a8d5.png">
  <p>Figure 3: Control signal and thrust characteristics</p>
</div>

<h2>Fail safe</h2>
The result of the trial includes the required output like
stop the boat using kill switch, switch ON and OFF control.

<h2>Failsafe working</h2>
<div align="center">
    <img src="https://user-images.githubusercontent.com/109530150/230298406-fc45ef1a-2e20-458a-b6e9-48dd01d471af.png">
  <p>Figure 4: Failsafe working</p>
</div>

The action of the boat is completely stopped with the
help of a kill switch. The connection of the kill switch process is
given above. If the boat is crashed, the kill switch can be used to
stop the boat. The failsafe signal is given to the receiver through
a dedicated radio channel.
It is detected through the sensor when the boat gets crashed or any
technical issue occurs. When the kill switch gets ON it stops the
boat completely and it turns the motor OFF. So, we can avoid
accidents and can handle any emergency situation by using a kill
switch in the boat.
<h2>Reset latch</h2>
Relays are energized thus maintaining the circuit in open state.
Once the power to the propulsion system is killed using any of
these modes, the boat cannot be driven again. Releasing of relay
latch using sperate switch is required for normal operation again.



