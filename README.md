<h1>Digital Logic Design Capstone Project</h1>

<h2>Description</h2>
The goal of this project was to design the automation required for an autonomous wheelchair to be able to navigate down a path without any intervention by the passenger. The portion of the autonomy designed for this project is the lateral movement of the wheelchair.
The synchronous sequential machines guiding the lateral movement will receive inputs that are designated to position the wheelchair to the left, right, or no lateral movement, and will be built as a 3-bit Mealy machine. The wheelchair will have a safety feature that keeps the lateral movement from moving more than 3 positions to the right or left.
For a 2-bit input Mealy machine, there is one extra ability that can be added to designate the 11 input, so a questionnaire to stakeholders was conducted to determine the best possible addition.
<br />


<h2>Design and Simulation Software Used</h2>

- <b>Digital</b><br><br>

<h2>Program walk-through:</h2>

<p align="center">
<b>Stakeholder Questionnaire:</b></p><br/>
<p align="left">
The stakeholder questionnaire included the following questions:<br><br>
  1. What does the extra 11 input correspond to?<br>
  2. What happens when the extreme locations are reached?(far left/far right)<br>
  3. What other safety features does the wheelchair need?<br>
  4. What kind of environment do you plan to use the design in?<br>
  5. What is your budget for purchasing an autonomous wheelchair?<br>

The solutions to the stakeholder questionnaire include the 11 input being a synchronous reset to the center lateral position, and when a right input in the extreme right position or left input in the extreme  left position are entered, the wheelchair will not move lateral in response to these inputs and will output a beeping alarm and warning light. An asynchronous reset to the center lateral position will be implemented later on in the development of the wheelchair.
The agreed-upon purchase price for the wheelchair was determined to be $5000, and the environments the wheelchair will operate in are homes, offices, sidewalks, hills, and inside stores. Two designs were implemented and scored based on design criteria, and the following design was the one chosen as the best fit because of its safety features.</p>
<br /> 
<br />
<p align="center">
<b>State Definition Table:</b><br><br/>
  <img src="https://i.imgur.com/BGAQXXl.png" height="80%" width="80%" alt="State Definition Table"/></p>
<br />
<br />
<p align="center">
<b>Input and Output Definition Tables:</b><br><br/>
  <img src="https://i.imgur.com/ZVCjyyK.png" height="50%" width="50%" alt="Input Definition Table"/>
  <img src="https://i.imgur.com/RYFqO7U.png" height="50%" width="50%" alt="Output Definition Table 1"/>
  <img src="https://i.imgur.com/a4eR7Lf.png" height="50%" width="50%" alt="Output Definition Table 2"/></p>
<br />
<br />
<br />
<p align="center">
<b>State Design Diagram:</b><br><br/>
  <img src="https://i.imgur.com/yZfoK2R.png" height="80%" width="80%" alt="State Design Diagram"/></p>
<br />
<br />
<br />
<p align="center">
<b>State Transition Table:</b><br><br/>
  <img src="https://i.imgur.com/2DFhv3I.png" height="80%" width="80%" alt="State Transition Table"/></p>
<br />
<br />
<br />
<p align="center">
<b>Karnaugh Maps:</b><br><br/>
  <img src="https://i.imgur.com/iH10XPH.png" height="80%" width="80%" alt="Karnaugh Map Q2 Q1"/>
  <img src="https://i.imgur.com/Riu6C3H.png" height="80%" width="80%" alt="Karnaugh Map Q0"/><br><br>
  <img src="https://i.imgur.com/F0lg1d3.png" height="80%" width="80%" alt="Karnaugh Map Z1 Z2"/><br><br><br>
  <img src="https://i.imgur.com/NdR2zy9.png" height="80%" width="80%" alt="Karnaugh Map Z3 Z4"/></p>
<br />
<br />
<br />
<p align="center">
<b>Design Equations:</b><br><br/></p>
<p align="left">
Design Equations:<br>
Q2+ = y’Q2 + x’Q2(Q1 + Q0) + xy’Q1’Q0’ <br>
Q1+ = x’y’Q1 + x’Q1(Q2’ + Q0) + x’yQ2’Q0 + xy’Q2(Q1 + Q0) + xy’Q1Q0 <br>
Q0+ = x’y’Q0 + xy’(Q2’Q1Q0’ + Q2Q1’Q0’) + x’y(Q1 + Q2’Q0’) <br>
Z1 = Q2Q1Q0’ <br>
Z2 = Q2’Q1Q0 <br>
Z3 = xy’Q2Q1Q0’ <br>
Z4 = x’yQ2’Q1Q <br></p>
<br />
<br />
<br />
<p align="center">
<b>Final Design in Digital Software:</b><br><br/>
  <img src="https://i.imgur.com/BptZGzW.png" height="110%" width="110%" alt="Final Design"/></p>
</p>
<br />
<br />
<br />
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
