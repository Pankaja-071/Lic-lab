## Lic-lab
## Experiment-1
<p>Common Source amplifier analysis</p><br>
<p>This experiment shows the ac,dc and transient analysis of cs amplifier </p>

## Abstract
<p>In this experiment, we study a Common Source Amplifier in three ways. First, we do DC analysis to check how the circuit behaves with a steady DC voltage and determine its biasing conditions. Next, we perform AC analysis to see how the amplifier responds to different frequencies. Finally, we conduct transient analysis to observe how the amplifier amplifies signals over time and measure its gain and output.</p>

## Theory
<p>  A Common-Source (CS) amplifier is a popular transistor amplifier configuration where the input is applied to the gate and the output is taken from the drain, with the source serving as the common terminal. It provides voltage amplification by modulating the drain current in response to changes in the gate-source voltage. The output is 180° out of phase with the input, and the amplifier has high input and output impedance.For a Common-Source (CS) amplifier to work correctly, the conditions are ,V <sub>GS</sub>≥V <sub>th</sub>(to turn the transistor on),V <sub>DS</sub>>V <sub> GS</sub><sub></sub> −V <sub>th</sub>(to keep the transistor in saturation),The input signal vin should be small for small-signal operation,Proper biasing and selection of 𝑅<sub>D</sub>are needed for stable operation and adequate voltage gain.
</p>
<p>In saturation region the current formula is given by I<sub>D</sub>=1/2k<sub>n</sub>V<sub>ov</sub></p><br>

##  circuit 1<br>

![image](https://github.com/user-attachments/assets/ac721cbe-63fb-4526-849b-4ee85b84f5b6)

<br>This circuit consists of a nmos transistor tsmc ,a resistor across drain and two voltage sourceseach connected to R<sub>d</sub> and gate terminal.<br>
<p>mosfet of lenth 180nm</p>
<p>mosfet of width 0.315um</p>
<p>voltage supply 1.8v</p>
<p>1k resistor </p>

## Dc Analysis
<p>The DC analysis of a Common-Source (CS) amplifier involves determining the biasing conditions of the transistor without considering the AC input signal. The gate-source voltage (V_GS) is set to ensure the transistor operates in the active region, typically by using a biasing network. The drain-source voltage (V_DS) is chosen to ensure the transistor remains in the saturation region. The drain current (I_D) is determined using the MOSFET's characteristic equation, with the source often being at ground or a reference voltage for proper bias stability. The DC analysis helps set the operating point (Q-point) of the transistor, ensuring linear operation when the AC signal is applied.</p>

![image](https://github.com/user-attachments/assets/67bb8fec-a50c-4825-8380-36c3298dd0a0)

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
    <td>1900um</td>
    <td>1500um</td>
    <td>10.92uA</td>
  </tr>
  <tr>
    <td>1900um</td>
    <td>1650um</td>
    <td>15.92uA</td>
  </tr>
  <tr>
    <td>1900um</td>
    <td>1700um</td>
    <td>17.89uA</td>
  </tr>
  <tr>
    <td>1900um</td>
    <td>1750um</td>
    <td>22.57uA</td>
  </tr>
  <tr>
    <td>1900um</td>
    <td>1750um</td>
    <td>25.2uA</td>
  </tr>
  <tr>
    <td>1900um</td>
    <td>1800um</td>
    <td>27.87uA</td>
  </tr>
</table>
<br>To check the mosfet is in saturation region 
<br>V<sub>ds</sub>=V<sub>d</sub>-V<sub>s</sub>
<br>
1.8-0=1.8v
<br>since V<sub>ds</sub>>V<sub>ov</sub>
<br>It is in saturation region
<br>The Q point is 1.8,27.87uA
<br>

## Transient Analysis
<br>
<p>The transient analysis of a Common-Source (CS) amplifier examines the amplifier's response to time-varying input signals. It focuses on how the transistor's drain current (I<sub>d</sub>) and output voltage (V<sub>out</sub>) change in response to small or large AC input signals. The input signal modulates the gate-source voltage (V<sub>gs</sub>), which affects the drain current (I<sub>d</sub>), creating an amplified output. The capacitances (like C<sub>gs</sub> and C<sub>ds</sub>) and resistive elements (like R<sub>d</sub>) determine the frequency response and time constants of the amplifier. The analysis shows how the amplifier amplifies signals while considering factors like rise time, fall time, and signal distortion</p>

# input transient analysis
![image](https://github.com/user-attachments/assets/e326de7a-2f4f-49f5-900b-ca326fdb63e0)

# output transient analysis
![image](https://github.com/user-attachments/assets/92f0aa95-ac12-460b-a799-0118eb211776)
<br>
<br><p>From the graph we can calculate the gain of the circuit.</p>
<br>A<sub>v</sub>sub>=V<sub>out</sub>/V<sub>in</sub>
<br>A<sub>v</sub>=1.772v / 950mV
<br>A<sub>v</sub>=1.8V/V
<br><p>which will match the theortical value calculated by A<sub>v</sub>=gmR<sub>d</sub></p>
<br>Where gm=K<sub>n</sub>V<sub>ov</sub>
<br><p>From graph we can clearly observe their is an 180 degree phase shift that is exibited by common souce configuration.</p>
<br><p>Therefore we can conclude that its gain > 1 and has 180 degree phase shift therefore its an NMOS common source amplifier.</p>

## AC Analysis        
<p>In the AC analysis of a common-source (CS) amplifier, the transistor is modeled as a voltage-controlled current source with transconductance 𝑔<sub>m</sub> , and the DC sources are replaced with short circuits. The voltage gain is approximately −𝑔<sub>m</sub> 𝑅<sub>D</sub>  , where 𝑅<sub>D</sub> is the drain resistance. If the output resistance  𝑟 <sub>o</sub> is considered, the voltage gain becomes −𝑔<sub>m</sub> 𝑅<sub>D</sub> /1+𝑔<sub>m</sub> 𝑟<sub>o</sub>  The input and output impedances are determined by resistances in the circuit, with the CS amplifier acting as a voltage amplifier.</p>
<p>In this AC analysis we will evaluate the frequency response cure of the given circuit.By applying the small analysis for the given circuit. In this Analysis we need to check in which frequency it act as a linear amplifier</p>
<p>While doing simulation we need to select the decade as type of sweep, with starting frequency as 0.1Hz and the stoping frequency as 1THz.</p>

![image](https://github.com/user-attachments/assets/f2ea00d7-0a02-4ea0-98f0-8af7b8fc9c30)
## Frequency response
<p> In this due to higher frequency the parasitic capacitor will get activated.</p>
<p>At lower frequency the coupling capacitors will get activated.</p>

## circuit 2

# theory
<p> A PMOS active load amplifier replaces the drain resistor with a PMOS transistor in the load, improving the amplifier's performance. The PMOS transistor acts as a constant current source, providing higher voltage gain and better linearity compared to a resistor. This configuration stabilizes the current and reduces distortion, making it ideal for amplifiers such as common-source or differential amplifiers, where it enhances the overall efficiency and signal accuracy.
</p>
<p>The drain current is obtained by formula :  I<sub>D</sub>=1/2k<sub>n</sub>V<sub>ov</sub</p>

![image](https://github.com/user-attachments/assets/d2740b32-a51b-4444-90f4-69d80291f78a)

## components details
<p>This circuit consist of two CMOS (NMOS and PMOS)tsmc, and two voltage source one at drain terminal of first MOSFET other at gate terminal of second MOSFET.</p>
<br>Mosfet length - 1.7um</br>
Mosfet width - 1.59um
<br>Supply voltage - 1.8v

## DC Analysis
<p>In the DC analysis of a PMOS active load amplifier, the focus is on determining the biasing conditions of the transistors. The PMOS transistor is biased in its active region, acting as a current source. The DC operating point (or bias point) of the amplifier is established by setting the gate-source voltages (V<sub>GS</sub) of both the active load (PMOS) and the input transistor (e.g., NMOS). The drain current is determined by the biasing voltages and the characteristics of the transistors, ensuring the PMOS transistor operates in its saturation region, providing a constant current for the load. This analysis is crucial for ensuring proper amplification in the active region.</p>
<p>DC Analysis is done to ensure the mosfet operates in saturation and to calculate the DC operating point of the transistor.This helps in getting a correct operating point despite the fluctuation in the other parameters.</p>

![image](https://github.com/user-attachments/assets/140a5079-65e0-40ff-a7ea-25b9c473feb3)

<V<sub>out</sub>=1.26V,<V<sub>in</sub>=0.6V,I<V<sub>d</sub>=27.11uA
<br>Given power dissipation is 100uW, then the current will be I<sub>d</sub>=Power/Voltage=27.11uA.</br>
<table>
  <tr>
    <td>Width(um)</td>
    <td>I<sub>d</sub>(uA)</td>
    <td>Vout(V)</td>
  </tr>
  <tr>
    <td>0.5u</td>
    <td>15.7</td>
    <td>0.56</td>
  </tr>
  <tr>
    <td>0.9u</td>
    <td>18.06</td>
    <td>0.962</td>
  </tr>
  <tr>
    <td>1.1u</td>
    <td>20.8</td>
    <td>1.04</td>
  </tr>
  <tr>
    <td>1.3u</td>
    <td>525.9</td>
    <td>1.15</td>
  </tr>
  <tr>
    <td>1.59u</td>
    <td>27.11u</td>
    <td>1.26V</td>
  </tr>
</table>
<br>V<sub>ds</sub>=V<sub>d</sub>-V<sub>s</sub>=1.26-0=1.26V</br>
<br>From the above calculation the operating point = (1.26V,27.11uA)</br>

## Transient analysis
<p>In the transient analysis of a PMOS active load amplifier, the focus is on the amplifier's response to time-varying input signals. The transient behavior is analyzed by considering how the signal fluctuates over time, affecting the voltages and currents through the transistors. The PMOS transistor, acting as an active load, provides a constant current that helps the circuit respond efficiently to input changes. The output signal is amplified based on the transistor's small-signal characteristics, with the PMOS load influencing the overall gain and bandwidth. Transient analysis helps assess the amplifier's dynamic performance, such as its ability to handle rapid signal variations without distortion.</p>

# input transient analysis
![image](https://github.com/user-attachments/assets/c8c7a2d6-c1e2-4183-b01e-c79e2650c95e)

# output transient analysis
![image](https://github.com/user-attachments/assets/5c45a713-0d34-4966-89af-b7207ba33de5)


From the graph we can calculate the gain of the circuit</br>
<br>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></br>
<br>A<sub>v</sub>=1.26V/880mV</br>
<br>A<sub>v</sub>=2.26V/V</br>
 ## AC Analysis
<br><p></p>AC Analysis is the small signal analysis of the circuit.This is done to determine the gain of the amplifier circuit.This also helps to analysis the frequency response of the amplifier circuit.The gain is given by A<sub>v</sub>=-g<sub>m</sub>R<sub>d</sub></p>

<br>During the process of AC simulation we need to select the decade as type of sweep, with starting frequency as 0.1Hz and the stoping frequency as 1THz.

![image](https://github.com/user-attachments/assets/4d57761f-0dba-4cb9-b713-3412ca8fd382)


## Frequency response:
<br>In this due to higher frequency the parasitic capacitor will get activated.
<br>At lower frequency the coupling capacitors will get activated.
## Inference
<br><p>*AC Analysis*: This deals with circuit powered by alternating current soources, where voltage and current change direction periodically. Analyzes steady state behaviour using phasor or representataion, impedance, and frequency response.</p>
<br><p>*DC Analysis*: It focuses on circuits powered by direct current sources, where voltage and current remain constant over time.Uses ohm's laws kirchhof's laws, and network theorems for solving circuit parameters</p>
*Transient Analysis*: 
Examines circuit behaviour during the transition from one steady state condition to another .Involves solving differential equations related to capacitors and inductors,which store and release energy.</p>

# Conclusion
<p>Our analysis confirmed that the amplifier works as expected, with proper biasing, frequency response, and signal amplification.</p>
