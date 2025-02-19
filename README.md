## Lic-lab
## Experiment-1
<p>Common Source amplifier analysis</p><br>
<p>This experiment shows the ac,dc and transient analysis of cs amplifier </p>
# Theory
<p>  A Common-Source (CS) amplifier is a popular transistor amplifier configuration where the input is applied to the gate and the output is taken from the drain, with the source serving as the common terminal. It provides voltage amplification by modulating the drain current in response to changes in the gate-source voltage. The output is 180° out of phase with the input, and the amplifier has high input and output impedance.For a Common-Source (CS) amplifier to work correctly, the conditions are ,V <sub>GS</sub>≥V <sub>th</sub>(to turn the transistor on),V <sub>DS</sub>>V <sub> GS</sub><sub></sub> −V <sub>th</sub>(to keep the transistor in saturation),The input signal vin should be small for small-signal operation,Proper biasing and selection of 𝑅<sub>D</sub>are needed for stable operation and adequate voltage gain.
</p>
<p>In saturation region the current formula is given by I<sub>D</sub>=1/2k<sub>n</sub>V<sub>ov</sub></p><br>
## circuit 1<br>
![image](https://github.com/user-attachments/assets/807fa28e-3b32-4661-ac03-e55b2ffb1903)
<br>This circuit consists of a nmos transistor tsmc ,a resistor across drain and two voltage sourceseach connected to R<sub>d</sub> and gate terminal.<br>
<p>mosfet of lenth 180nm</p>
<p>mosfet of width 0.315um</p>
<p>voltage supply 1.8v</p>
<p>1k resistor </p>
## Dc Analysis
<p>The DC analysis of a Common-Source (CS) amplifier involves determining the biasing conditions of the transistor without considering the AC input signal. The gate-source voltage (V_GS) is set to ensure the transistor operates in the active region, typically by using a biasing network. The drain-source voltage (V_DS) is chosen to ensure the transistor remains in the saturation region. The drain current (I_D) is determined using the MOSFET's characteristic equation, with the source often being at ground or a reference voltage for proper bias stability. The DC analysis helps set the operating point (Q-point) of the transistor, ensuring linear operation when the AC signal is applied.</p>
![image](https://github.com/user-attachments/assets/abc5d9ce-6ab4-4ffb-aef7-57f9ebe62a4f)
<br>From this simulation V<sub>out</sub=1.693,V<sub>in</sub>=0.9v and I<sub>d</sub>=5.5A<br>
the load line equation is given by V<sub>out</sub>=V<sub>dd</sub>-I<sub>d</sub>R<sub>d</sub>
The calculated value does not match with simulated one so we will change the width to maintain the length at 180nm to desired current value.<br>
<table>
  <tr>
    <td>Length</td>
    <td>Width</td>
    <td>I<sub>d</sub></td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.1um</td>
    <td>10.92uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.15um</td>
    <td>28.92uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.2um</td>
    <td>38.89uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.25um</td>
    <td>44.57uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.3um</td>
    <td>49.2uA</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>0.38um</td>
    <td>51.69uA</td>
  </tr>
</table>
<br>To check the mosfet is in saturation region 
<br>V<sub>ds</sub>=V<sub>d</sub>-V<sub>s</sub>
<br>
1.8-0=1.8v
<br>since V<sub>ds</sub>>V<sub>ov</sub>
<br>It is in saturation region
<br>The Q point is 1.8,51.69uA
<br>
## Transient Analysis
<br>
<p>The transient analysis of a Common-Source (CS) amplifier examines the amplifier's response to time-varying input signals. It focuses on how the transistor's drain current (I<sub>d</sub>) and output voltage (V<sub>out</sub>) change in response to small or large AC input signals. The input signal modulates the gate-source voltage (V<sub>gs</sub>), which affects the drain current (I<sub>d</sub>), creating an amplified output. The capacitances (like C<sub>gs</sub> and C<sub>ds</sub>) and resistive elements (like R<sub>d</sub>) determine the frequency response and time constants of the amplifier. The analysis shows how the amplifier amplifies signals while considering factors like rise time, fall time, and signal distortion</p>



<br>
<br><p>From the graph we can calculate the gain of the circuit.</p>
<br>A<sub>v</sub>sub>=V<sub>out</sub>/V<sub>in</sub>
<br>A<sub>v</sub>=1.75v / 950mV
<br>A<sub>v</sub>=1.8V/V
<br><p>which will match the theortical value calculated by A<sub>v</sub>=gmR<sub>d</sub></p>
<br>Where gm=K<sub>n</sub>V<sub>ov</sub>
<br><p>From graph we can clearly observe their is an 180 degree phase shift that is exibited by common souce configuration.</p>
<br><p>Therefore we can conclude that its gain > 1 and has 180 degree phase shift therefore its an NMOS common source amplifier.</p>
<br>*AC Analysis*</br>         

