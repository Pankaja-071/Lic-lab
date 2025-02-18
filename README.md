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
