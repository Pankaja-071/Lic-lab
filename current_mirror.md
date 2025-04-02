## Current Mirror
<p>A current mirror is an electronic circuit that replicates a reference current at its output, ensuring a stable and predictable current source. It typically consists of two or more matched transistors, where one transistor sets the reference current and the others mirror it. Current mirrors are widely used in analog circuits for biasing, amplification, and signal processing, offering high accuracy and stability. Variants like the Wilson and cascode current mirrors enhance performance by improving output resistance and reducing errors. Common in integrated circuits, current mirrors play a crucial role in maintaining consistent current flow in amplifiers, voltage regulators, and differential pairs.</p>

## Part A
## <p>Design and analysis current mirro circuit as active load in amplifier circuit for A<sub>v</sub>>-10V/V, V<sub>dd</sub>=1.8V, P<1mW.</p>

 ## circuit-1
<p><b>This circuit's simulation is done for 1:1 aspect ratio</b></p>

![p1 c1 1 ckt](https://github.com/user-attachments/assets/765fd686-f537-4311-9b48-8e6b62a38de7)
<p>I<sub>total</sub>=(power/V<sub>dd</sub>)</p>
<p>=(1m/1.8)</p>
=0.5mA
<p>I<sub>ref</sub>=I<sub>d</sub>=(I<sub>total</sub>/2)</p>
<p>=0.5m/2</p>
=0.27mA

## DC Analysis

![p1 c1 1 width](https://github.com/user-attachments/assets/a500fe51-5794-4018-9862-30f4ded5ba34)<br>

![p1 c1 1 dc pt](https://github.com/user-attachments/assets/1d7677a3-d5a6-4299-a433-be345b7a04f5)<br>
![p1 c1 1 additional](https://github.com/user-attachments/assets/97983980-bf03-4d5a-bc70-e52204be48d3)<br><br>


<p>The DC analysis of a current mirror circuit involves determining the reference current and analyzing how accurately it is mirrored at the output. In a basic BJT current mirror, the reference current is set by an external resistor and flows through a diode-connected transistor, establishing a base-emitter voltage. An identical transistor copies this current. However, practical factors like transistor mismatch, base currents, and the Early effect introduce minor deviations. Similarly, in a MOSFET current mirror, the gate-source voltage determines current mirroring, but channel length modulation can affect accuracy. Advanced designs like the Wilson and cascode current mirrors improve precision by increasing output resistance and reducing systematic errors.</p>
<p>MOSFET length - 180nm</p>
<p>width of M3- 101um</p>
<p>V<sub>out</sub> = 1.162v </p>
<p>The above circuit is in saturation region that is V<sub>ds</sub>>V<sub>gs</sub>-V<sub>th</sub>.</p>

## Transient Analysis

![p1 c1 1 ac input](https://github.com/user-attachments/assets/1c148b74-db77-4a23-a699-42deaaa3016d)
![p1 c1 1 ac output](https://github.com/user-attachments/assets/637410f4-0ab0-4b28-80ca-e68c24f5e9ec)


<p>The transient analysis of a current mirror examines its response to time-varying signals and how quickly it stabilizes to mirror the reference current. When power is first applied, the transistors undergo a brief settling time as the base-emitter (or gate-source) voltages adjust to establish the desired current. During this phase, capacitive effects in the transistors, such as junction capacitances and stray parasitics, influence the circuit’s speed and stability. In BJTs, base charging delays can cause a short overshoot or undershoot in I<sub>out</sub>, while in MOSFETs, gate capacitance affects the transition speed. To improve transient performance, techniques like adding compensation capacitors or using active feedback circuits can help reduce settling time and enhance stability.</p>
<p>The input voltage given is 0.5V and amplitude of 1mV and frequency of 1KHz</p>
<p>The output voltage can be observed as 1.162V</p>

## AC Analysis
<p>The AC analysis of a current mirror focuses on its small-signal behavior, particularly output impedance and frequency response. Ideally, the output impedance should be high for effective current mirroring, but practical limitations like channel length modulation reduce it. At higher frequencies, parasitic capacitances, such as gate-drain and drain-substrate capacitances, introduce phase shifts and affect stability. These factors limit the bandwidth and accuracy of current mirroring. To improve AC performance, techniques like cascode configurations or gain-boosted mirrors are used to increase output impedance and minimize frequency-dependent distortions.</p>

![p1 c1 1 ac analysis](https://github.com/user-attachments/assets/d4c72c82-aa2c-4363-8d79-32b9057f7d6a)
![p1 c1 1 max](https://github.com/user-attachments/assets/4393ee65-64c4-43b6-b3a2-5abdcc3d6df2)

<p>The gain from above simulation is 23.15d<sub>B</sub>.</p>
<p>The 3d<sub>B</sub> gain is 20.15 and the frequency of this gain is 49.53MHz.</p>

## 1:1 aspect ratio.
## comparision table for different length 
<p><b>Length=180nm</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
  <td>I<sub>d</sub>1(mA)</td>
  <td>I<sub>d</sub>2(mA)</td>
  <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
  <td>55</td>
  <td>55</td>
  <td>101</td>
  <td>0.27</td>
  <td>0.27032</td>
  <td>0.27032</td>
 </tr>
 <tr>
  <td>55</td>
  <td>55</td>
  <td>110</td>
  <td>0.27</td>
  <td>0.2768</td>
  <td>0.2768</td>
 </tr>
 <tr>
  <td>55</td>
   <td>55</td>
   <td>90</td>
   <td>0.27</td>
   <td>0.2598</td>
  <td>0.2598</td>
 </tr>
</table>

![p1 c1 1 width](https://github.com/user-attachments/assets/a500fe51-5794-4018-9862-30f4ded5ba34)<br>

![p1 c1 1 dc pt](https://github.com/user-attachments/assets/1d7677a3-d5a6-4299-a433-be345b7a04f5)<br>


<p><b>Length=500um</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
  <td>I<sub>d</sub>1(mA)</td>
    <td>I<sub>d</sub>2(mA)</td>
    <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
  <td>55</td>
   <td>55</td>
   <td>190</td>
   <td>0.27</td>
   <td>0.2703</td>
   <td>0.2703</td>
 </tr>
 <tr>
  <td>55</td>
    <td>55</td>
    <td>180</td>
    <td>0.27</td>
   <td>0.2642</td>
   <td>0.2642</td>
 </tr>
 <tr>
  <td>55</td>
  <td>55</td>
  <td>200</td>
  <td>0.27</td>
  <td>0.2752</td>
    <td>0.2752</td>
 </tr>
</table>


![p1 c2 ckt](https://github.com/user-attachments/assets/f8e0f4d9-b647-4a0e-9e7b-d9045ea5e7f2)

![p1 c1 1 500n 1](https://github.com/user-attachments/assets/e0815bae-c5eb-47e1-b188-7b8253427a18)


<p><b>Length=1um</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
    <td>I<sub>d</sub>1(mA)</td>
    <td>I<sub>d</sub>2(mA)</td>
    <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
  <td>55</td>
   <td>55</td>
   <td>227</td>
   <td>0.27</td>
  <td>0.27002</td>
  <td>0.27002</td>
 </tr>
 <tr>
  <td>55</td>
  <td>55</td>
  <td>220</td>
  <td>0.27</td>
  <td>0.2669</td>
  <td>0.2669</td>
 </tr>
 <tr>
  <td>55</td>
    <td>55</td>
    <td>230</td>
    <td>0.27</td>
    <td>0.2711</td>
  <td>0.2711</td>
 </tr>
</table>


![p1 c1 1 1u 2](https://github.com/user-attachments/assets/4e218d16-9eb9-4f77-b4f0-d12b62c36a68)
![p1 c1 1 1u 1](https://github.com/user-attachments/assets/63d2aafb-917a-49f1-8675-f24ba93a332b)



## Circuit-2
<p><b>This circuit simulation is done for 1:2 aspect ratio.</b></p>

![p1 c1 1 ckt](https://github.com/user-attachments/assets/4741cb46-127d-427e-87a9-73ead8e59cda)


## DC Analysis
In a 1:2 aspect ratio current mirror, the output transistor is sized twice as large as the reference transistor, leading to an output current that is ideally twice the reference current. Since both transistors share the same gate-source voltage, the drain current equation scales with the width-to-length ratio. Given that the output transistor has twice the aspect ratio, it produces I<sub>out</sub>=2I<sub>ref</sub>, making this configuration useful for current scaling in analog and integrated circuits.

![p1 c1 2 dc](https://github.com/user-attachments/assets/9c4cb24a-50c1-4575-858d-8f6f5495d928)
![p1 c1 2 additional](https://github.com/user-attachments/assets/4400d07e-e93b-41d1-9da7-1e9f47025ba7)


<p>From above simulation we can see that the V<sub>out</sub> is 1.1916V</p>
<p>MOSFET Length-180nm</p>
<p>Width of M3-118um</p>
<p>I<sub>0.32mA</sub></p>

## Transient Analysis

<p>In a 1:2 aspect ratio current mirror, the transient response is influenced by the larger output transistor's increased gate capacitance, which affects the circuit’s settling time. When power is applied or a sudden change occurs, the gate voltage  must stabilize, and the larger transistor may introduce a slight delay due to its increased capacitance. This can cause a brief overshoot or undershoot in I<sub>out</sub> before it settles to 2I<sub>ref</sub>. To improve transient performance, techniques like reducing parasitic capacitances or using a compensation network can help achieve faster stabilization and minimal delay.</p>
<p><b>Input voltage </b></p>

![p1 c1 2 input](https://github.com/user-attachments/assets/34c329a0-b66e-4c0e-8bb5-829be8107e6a)

<p><b>Output voltage</b></p>

![p1 c1 2 output](https://github.com/user-attachments/assets/a35bcd0c-632d-4ea7-a1a5-8b69f148a96e)

<p>The input voltage given is 0.5V and amplitude of 1mV and frequency of 1KHz</p>

## AC Analysis
<p>In a 1:2 aspect ratio current mirror, the AC analysis focuses on output impedance and frequency response. The larger output transistor has twice the width, reducing its small-signal output resistance due to increased channel length modulation effects. Additionally, the increased gate-drain and drain-substrate capacitances introduce more parasitic effects, slightly lowering the bandwidth. As a result, the mirror’s frequency response is affected, with a potential decrease in high-frequency performance.</p>

![p1 c1 2 ac](https://github.com/user-attachments/assets/b26f6f11-af54-481b-863b-572cee235aed)

<p>From above simulation the gain is 22.88d<sub>B</sub> and the 3d<sub>B</sub> gain is 19.88</p>
<p>The frequency of this gain is 34.15MHz</p>

![p1 c1 2 max](https://github.com/user-attachments/assets/34e00f22-e3ff-434c-b1b5-e0d10c7bfc71)
![p1 c1 2 band](https://github.com/user-attachments/assets/834c0197-4e19-4af4-9c31-0153430b0412)


## Aspect ratio 1:2
## comparision table for different length

<p><b>Length=180nm</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
    <td>I<sub>d</sub>1(mA)</td>
    <td>I<sub>d</sub>2(mA)</td>
    <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
  <td>55</td>
   <td>110</td>
   <td>110</td>
   <td>0.16</td>
  <td>0.312</td>
  <td>0.312</td>
 </tr>
<tr>
 <td>55</td>
   <td>110</td>
   <td>100</td>
   <td>0.16</td>
  <td>0.30058</td>
  <td>0.30058</td>
</tr>
 <tr>
   <td>55</td>
   <td>110</td>
   <td>90</td>
   <td>0.16</td>
  <td>0.2850</td>
  <td>0.28502</td>
 </tr>
 <tr>
   <td>55</td>
   <td>110</td>
   <td>118</td>
   <td>0.16</td>
  <td>0.320094</td>
  <td>0.320094</td>
 </tr>
 <tr>
   <td>55</td>
   <td>110</td>
   <td>125</td>
   <td>0.16</td>
  <td>0.3258</td>
  <td>0.3258</td>
 </tr>
</table>

![p1 c1 2 dc](https://github.com/user-attachments/assets/9c4cb24a-50c1-4575-858d-8f6f5495d928)
![p1 c1 2 additional](https://github.com/user-attachments/assets/4400d07e-e93b-41d1-9da7-1e9f47025ba7)

<p><b>Length=500um</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
    <td>I<sub>d</sub>1(mA)</td>
    <td>I<sub>d</sub>2(mA)</td>
    <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
   <td>55</td>
   <td>110</td>
   <td>222.5</td>
   <td>0.16</td>
  <td>0.32006</td>
  <td>0.32006</td>
 </tr>
 <tr>
  <td>55</td>
   <td>110</td>
   <td>200</td>
   <td>0.16</td>
  <td>0.3027</td>
  <td>0.3027</td>
 </tr>
 <tr>
  <td>55</td>
   <td>110</td>
   <td>230</td>
   <td>0.16</td>
  <td>0.3243</td>
  <td>0.3243</td>
 </tr>
</table>

![p1 c1 2 500n](https://github.com/user-attachments/assets/cb5f391f-0e4a-4be4-a023-cc87f4fba8fe)

<p><b>Length=1um</b></p>
<table>
 <tr>
  <td>M1 W(um)</td>
  <td>M2 W(um)</td>
  <td>M3 W(um)</td>
    <td>I<sub>d</sub>1(mA)</td>
    <td>I<sub>d</sub>2(mA)</td>
    <td>I<sub>d</sub>3(mA)</td>
 </tr>
 <tr>
  
  <td>55</td>
   <td>110</td>
   <td>268</td>
   <td>0.16</td>
  <td>0.3208</td>
  <td>0.3208</td>
 </tr>
 <tr>
  <td>55</td>
   <td>110</td>
   <td>250</td>
   <td>0.16</td>
  <td>0.31103</td>
  <td>0.31103</td>
 </tr>
 <tr>
   <td>55</td>
   <td>110</td>
   <td>280</td>
   <td>0.16</td>
  <td>0.3256</td>
  <td>0.3256</td>
 </tr>
</table>


![p1 c1 2 1u](https://github.com/user-attachments/assets/24b85e26-4049-42de-b135-af96011a506c)





## Part B
<p>Design the differential amplifier using the same design specifications as differential amplifier  experiment(exp-3). perform DC analysis, Transient , AC Anslysis for the circuit</p>

![p1 c2 ckt](https://github.com/user-attachments/assets/cf1a9e5d-2f95-403b-9d68-1308e967ad38)


<p>This CMOS differential amplifier consists of six MOSFETs (M1–M6) designed to amplify differential signals while rejecting common-mode noise. The NMOS transistors (M2 and M6) form the differential input stage, while M4 and M5 create a current mirror to ensure proper biasing. The PMOS transistors (M1 and M3) act as active loads, enhancing gain. A constant current source (I1) provides biasing, and voltage sources (V3 and V4) supply 2.2V power. Differential input signals with a 180-degree phase shift are applied through V1 and V2. This amplifier is widely used in analog signal processing, offering high gain and noise rejection capabilities.</p>

## DC Analysis

![current2part dc opt2](https://github.com/user-attachments/assets/2619b502-d6db-4bde-9cb0-9fa2542421c9)

![current2part dc opt](https://github.com/user-attachments/assets/1dcb031b-79be-40fe-8573-3c3718a3c48f)


<p>The DC analysis of this CMOS differential amplifier determines the biasing conditions and operating points of the transistors. The tail current source (I1) sets a stable bias current, which splits between the NMOS differential pair (M2 and M6) based on the input voltage difference. The PMOS transistors (M1 and M3) act as active loads, operating in saturation to provide high impedance and enhance gain. A current mirror (M4 and M5) ensures balanced operation by maintaining equal current flow through M2 and M6. The DC voltage at the output node (Vout) is influenced by the drain voltage of M1 and M3, ensuring proper signal amplification while rejecting common-mode noise.</p>

<p>MOSFET Length-180nm</p>
<p>Width of M2 and M6-27.008um</p>
<p>V<sub>out</sub>=0.6432V/p>

## Transient Analysis

![current2part transient](https://github.com/user-attachments/assets/3c34c537-2a1d-4ed0-ab67-1c33d2ab7459)

<p>The transient analysis of this CMOS differential amplifier examines its time-domain response to varying input signals. The differential inputs (V1 and V2) are sinusoidal signals with a 180-degree phase shift, causing the NMOS differential pair (M2 and M6) to alternately conduct. This variation is mirrored in the current through the PMOS active loads (M1 and M3), generating an amplified output voltage (Vout). The response time and stability of the circuit depend on the biasing current (I1) and transistor parameters. The transient analysis helps evaluate signal amplification, phase shift, and dynamic performance, ensuring proper operation for analog signal processing applications.</p>
<p>From above simulation V<sub>out</sub> is 670mV. </p>

## AC Analysis

![current2part ac analysis](https://github.com/user-attachments/assets/ba4280e5-c1d4-4ff8-8adc-76e6415382ff)
<p>The AC analysis of this CMOS differential amplifier, as shown in the provided frequency response plot, evaluates the gain and phase characteristics over a wide frequency range. The Bode plot displays the gain (in dB) and phase (in degrees) of the output voltage \( V_{out} \). At low frequencies, the amplifier maintains a relatively stable gain before experiencing a gradual roll-off at higher frequencies due to parasitic capacitances and transistor limitations. The phase shift transitions from 0° at low frequencies to -180° at high frequencies, indicating the frequency-dependent behavior of the amplifier. The -3dB bandwidth, observed around several MHz, defines the effective operating range of the circuit. This analysis helps in determining the amplifier’s suitability for high-frequency applications by assessing its gain stability and phase response over a broad spectrum.</p>

## Result
<p>The first circuit demonstrates a current mirror with a 1:2 aspect ratio, where the width-to-length ratio of the transistors is adjusted to control the mirrored current. The reference current (I1) is set to 0.16 mA, and the circuit is biased with a 1.8V supply. The AC analysis setup indicates that the frequency response of the circuit is being analyzed, and transient simulations help observe the dynamic behavior. The output current is expected to be twice the reference current due to the aspect ratio difference. This design ensures an amplified current while maintaining stability, making it suitable for circuits requiring higher output currents while referencing a smaller bias current.

The second circuit operates with a 1:1 aspect ratio, meaning the mirrored current is expected to be equal to the reference current. Here, the reference current (I1) is 0.27 mA, and the circuit runs under the same 1.8V supply. Since both transistors have identical dimensions, the output current should ideally match the reference current. This configuration ensures a direct and accurate current replication, minimizing deviations caused by mismatched transistors. The DC operating point analysis shows power dissipation and current flow, verifying proper circuit function.

The third circuit is an advanced current mirror setup similar to the previous configurations but with an active load and differential pair configuration. This design operates with a 2.2V supply and includes multiple MOSFETs configured for differential input operation. The AC and transient analysis results highlight an improved gain and better frequency response due to the active load implementation. The circuit is designed to handle differential signals, improving noise rejection and making it more efficient for analog signal processing applications.

Overall, the different aspect ratios affect the output current, gain, and power dissipation. The 1:2 ratio scales the current, the 1:1 ratio maintains accurate mirroring, and the differential configuration with an active load improves amplification and response characteristics. These findings are crucial for designing precise and efficient analog circuits in modern integrated circuit applications.</p>

## Inference:
From the above experimental observations, it is evident that the aspect ratio of MOSFETs in a current mirror plays a crucial role in determining the output current.  

1. Impact of Aspect Ratio on Current Mirroring:  
   - In the 1:2 aspect ratio circuit, the output current is twice the reference current, validating the theoretical expectation that increasing the width of the output transistor leads to proportional current scaling. This configuration is useful when a higher mirrored current is needed while using a small reference current.  
   - In the 1:1 aspect ratio circuit, the mirrored current is nearly identical to the reference current, which is ideal for maintaining precise current replication. This setup is preferred for applications requiring accuracy and minimal current mismatch.  

2. DC Operating Point and Power Dissipation: 
   - The second circuit showed a higher reference current (0.27 mA), which resulted in increased power dissipation. The power dissipation depends on both the reference current and supply voltage, meaning higher current levels can lead to greater thermal effects in practical applications.  

3. Improved Performance with Differential Configuration:
   - The third circuit, incorporating a differential pair and active load, exhibits better gain and frequency response characteristics.  
   - The use of differential inputs helps in noise rejection and improved signal processing, making this setup more suitable for high-precision analog applications such as operational amplifiers and sensor interfaces.  

4. Design Considerations: 
   - The choice of aspect ratio and circuit configuration depends on the application requirements—whether current amplification, precision, or differential operation is the primary goal.  
   - Mismatches in transistor characteristics, process variations, and temperature changes may introduce small errors in current mirroring, which need to be considered in practical implementations.  

### Conclusion:  
The experiments confirm that the aspect ratio of transistors directly influences current mirroring  accuracy and gain. The 1:2 ratio provides current amplification, while the 1:1 ratio ensures accurate mirroring. The differential current mirror with an active load improves frequency response and gain, making it ideal for advanced analog applications. These findings are essential for designing efficient current mirrors in analog IC design.
