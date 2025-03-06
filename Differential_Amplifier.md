## Lic-lab
## Experiment-3
<p>Differential amplifier analysis</p><br>
<p>This experiment shows the ac,dc and transient analysis of Differential amplifier </p><br>
<p>Question : Design Differential amplifier for the following specifications vdd=2.5v ,vicm=1.3v ,vocm=1.4v, vp=0.5v. Perform Dc analysis, transient analysis, frequency response and extract the required parameters.</p><br>

![IMG_20250306_111047](https://github.com/user-attachments/assets/b9440e5f-9ce8-491f-911c-5ba7b42cfbde)

## Abstract
<p> We need to design a differential amplifier that meets specific voltage and input signal criteria. The design process involves performing four essential analyses: DC Analysis to establish the amplifier's operating point, Transient Analysis to observe its response to varying signals, Frequency Response Analysis to evaluate its performance across a range of frequencies, and Parameter Extraction to collect critical information like gain and bandwidth. Additionally, we need to determine the input and output swing of the amplifier. The objective is to ensure the amplifier operates optimally within the defined specifications.
</p>

##Theory

<p>A differential amplifier is an electronic device specifically designed to amplify the voltage difference between two input signals, providing high accuracy and noise immunity. It has two inputs: a non-inverting input and an inverting input. The amplifier boosts the voltage difference between these two inputs while rejecting any voltage that is common to both, referred to as the common-mode voltage. <br>
 This ability to reject common-mode signals is quantified by the common-mode rejection ratio (CMRR), which measures the amplifier's effectiveness in ignoring noise or interference that affects both inputs equally. Differential amplifiers are widely used in applications such as signal processing, instrumentation, and communication systems, where it is essential to amplify weak signals in the presence of noise or other unwanted interference. By focusing only on the difference between the two inputs, differential amplifiers can effectively filter out external disturbances, making them invaluable in environments with high levels of electromagnetic interference. <br>
 
 For example, in medical instrumentation like electrocardiogram (ECG) machines, differential amplifiers help isolate the small electrical signals from the heart while rejecting noise from other sources. Similarly, in communication systems, they ensure that the desired signal is amplified while minimizing the effect of common-mode noise, ensuring clear and reliable signal transmission.
</p>

![17412325438756253492796588430102](https://github.com/user-attachments/assets/a7f5255d-0e60-4c25-9ab6-ad3db0235aa2)

<p>A differential amplifier amplifies the difference between two input voltages—V₁ (non-inverting) and V₂ (inverting)—and provides an output that is proportional to this difference. The key feature is its common-mode rejection ratio (CMRR), which quantifies how well the amplifier rejects signals that are common to both inputs. A high CMRR means the amplifier is effective at rejecting noise or interference that affects both inputs equally.</p>

# circuit 1
![pckt 1](https://github.com/user-attachments/assets/ded18a03-5936-4a46-af1f-4a0cfb53b90a)

<p>This circuit consists of two nmos transistors ,3 resistors 2 voltage sources and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.8k ohm</p>
<p>rss of 416.66 ohm</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

#  Dc analysis
<p>The DC analysis of a differential amplifier involves determining the biasing conditions of the circuit when no input signal is applied (i.e., with a constant DC voltage). This analysis helps set the operating point of the transistors, ensuring they work in their active region. Key parameters like the quiescent currents, voltages across components, and the overall stability of the circuit are determined. DC analysis is essential for setting the proper biasing to ensure the amplifier functions correctly when signals are later applied.</p>

![pckt1 dc op](https://github.com/user-attachments/assets/a01ece25-dafc-42d4-9855-e7be7e9268d0)

![pckt1 lenwid](https://github.com/user-attachments/assets/b01497d5-ae9d-4002-883a-92358a6feba8)


<br>
<p>This  differential amplifier circuit has two resistors each of 1.8k,two voltage source of 1.3v,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=7.918um</p>
<p>Q point is(1.4v,0.6mA)</p>
<br>

![pckt1 additional](https://github.com/user-attachments/assets/eeaf0fc5-46ed-46d4-8636-452dc56fd76b)
<p>The above image shows the other parameters of the mosfet like v<sub>gs</sub>,v<sub>t</sub> ,g<sub>m</sub> v<sub>ds</sub> and others</p>
<br>

# Transient analysis

<p>Transient analysis of a differential amplifier studies how the circuit responds to changes in the input signal over time. It simulates the amplifier’s behavior when the input voltage suddenly changes, such as when a pulse or step input is applied. This analysis helps determine how quickly the amplifier can respond, including how long it takes to reach a stable output, known as rise time, fall time, and settling time. It ensures the amplifier can accurately amplify signals without distortion or delays when dealing with real-time, rapidly changing inputs.</p>
<p>Transient analysis of Input</p>  
<br>

![pckt1 tran ip](https://github.com/user-attachments/assets/26552f13-e8d7-4c5e-9983-44e736b249b4)
<p>Transient analysis of output</p>  
<br>

![pckt1 tran op](https://github.com/user-attachments/assets/73608594-950a-4d91-b11f-62a14d20c414)
<p>Transient analysis of both input and output</p>
<br>

![pckt 1 tran inout](https://github.com/user-attachments/assets/c587ccf4-30ed-4798-bcb1-2e81aee51438)

<br>
<p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.34401-1.2557=0.08831</p>
<p>V<sub>out</sub>=1.4737-1.347=0.1267</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.1267/0.08831=1.434 V/V</p>
<br>

# Ac analysis

<p> AC analysis of a differential amplifier looks at how the amplifier responds to changing input signals, like alternating current (AC) signals. It helps determine how much the amplifier amplifies the input signal (gain) and how well it performs across different frequencies. This analysis shows the frequency response, such as the bandwidth and cutoff points, which indicates how effectively the amplifier handles high or low-frequency signals. Essentially, AC analysis helps ensure the amplifier works well with real-world, time-varying signals.</p>
<p>Ac analysis</p>
<br>

![pckt1 ac](https://github.com/user-attachments/assets/109a1cfb-e9f3-4c64-b0b3-60b38fba057a)

![pckt1 max a](https://github.com/user-attachments/assets/26037b75-956b-4516-9a6c-354c266045f3)

<br><p>From the above figure we can note the maximum gain in db </p>
<p>A<sub>v</sub> in db=1.35db</p>
<br>

![pckt1 bw](https://github.com/user-attachments/assets/a171e3f5-99ff-4f59-9f25-f6e6b8f8e1b3)

<br><p>Gain remains constant as their is no change in R<sub>d</sub>.From the above smulation the maximum frequency range is 7.899GHz and low frequency range is 100MHz.</p>
 <p>The bandwidth of this circuit is BW = f<sub>h</sub>-f<sub>l</sub></p>
 <p>BW= 7.899GHz-100mHz =7.899 GHz</p>
<br>


# Input swing
<p>The input swing of a differential amplifier refers to the range of input voltages over which the amplifier can operate correctly without distortion. It represents the minimum and maximum input voltages that can be applied to the amplifier's inputs while still allowing it to produce an accurate output. If the input signal goes beyond this range, the amplifier may enter saturation or cutoff, causing the output to be distorted or clipped. The input swing is important for ensuring the amplifier can handle varying input signals without losing performance.</p>
<p>The DC offset here is done by taking the average of V<sub>in min</sub> and V<sub>in max</sub></p>
<p>V<sub>in min</sub>=V<sub>t N</sub> + V<sub>p</sub></p>
<p>V<sub>in max</sub>=V<sub>dd</sub>-R<sub>d</sub>I<sub>ss</sub>/2 = V<sub>t</sub></p><br>
<br>

# circuit 2
<p>In this circuit we have replaced the resistor with a current source with I<sub>ss</sub>=1.2mA</p>

![Screenshot 2025-03-05 185934](https://github.com/user-attachments/assets/230a129f-a325-4b58-8147-e5248e454678)

<p>This circuit consists of two nmos transistors ,2 resistors 2 voltage sources ,a current source and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.827k ohm</p>
<p>Iss of 1.2mA</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

#  Dc analysis

![Screenshot 2025-03-05 185934](https://github.com/user-attachments/assets/3834dbe1-7f16-4d25-87a4-3baff89c6d34)<br>

![Screenshot 2025-03-05 173453](https://github.com/user-attachments/assets/b861e2eb-5e05-49c7-b414-4a8a49b4c6e2)<br>
<br><p>This  differential amplifier circuit has two resistors each of 1.827k,two voltage source of 1.3v,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=7.9um</p>
<p>Q point is(1.4v,0.6mA)</p>
<br>

![Screenshot 2025-03-05 190025](https://github.com/user-attachments/assets/dcbcb1b7-49fe-4434-b66b-57572a8bf1ab)<br>



 #  Transient analysis
 
 <p>Transient analysis of Input</p>  
 
 ![Screenshot 2025-03-05 204422](https://github.com/user-attachments/assets/3434631d-1e61-4e29-a4af-4addb5ecba03)
 <p>Transient analysis of output</p>  
 
 ![Screenshot 2025-03-05 204340](https://github.com/user-attachments/assets/093c8c3b-f4df-4ba7-a558-d17492e86cdf)
 <br>
 <p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.3495-1.212=0.1375</p>
<p>V<sub>out</sub>=1.4080031-1.4079965=0.0000066</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.0000066/0.13495=0.0074 V/V</p>
<br>

 
# Ac analysis
<p>AC analysis of a differential amplifier focuses on evaluating its response to small input signals. It determines the differential gain, input and output impedance, and common-mode rejection ratio (CMRR). The amplifier amplifies the voltage difference between the two inputs while rejecting common-mode noise. Key factors influencing performance include the transistor’s transconductance and load resistance. The analysis also considers the frequency response, which is affected by parasitic capacitances. This helps in optimizing the amplifier’s performance in applications requiring noise immunity and precise signal amplification.
<p>The dc offset value is 1.3v , amplitude is 50m,and frequency is 1KHZ</p>

![Screenshot 2025-03-05 210453](https://github.com/user-attachments/assets/3f5e50fe-8c97-4e81-bbe9-8f2a307d1278)

<br>
<br>


# circuit 3
<p>In this circuit we have replaced the resistor with a nmos transistor and the voltage v<sub>b</sub>is 0.86v</p>
<p> V<sub>b</sub>= V<sub>t</sub>+ V<sub>p</sub> </p>
<p> V<sub>b</sub>= 0.36+0.5=0.86</p>

![pckt3](https://github.com/user-attachments/assets/176edeb5-d6b8-4635-b99f-d3711137a609)

<p>This circuit consists of three nmos transistors ,2 resistors 3 voltage sources and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.81k ohm</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

![pckt 3 additional](https://github.com/user-attachments/assets/2171d6fd-15be-4e97-80e7-fed8455a0d96)


#  Dc analysis

![pckt3 dc op](https://github.com/user-attachments/assets/532c45f3-65bb-4d77-8c4c-3f9b3070755f)
![pckt3 lewe](https://github.com/user-attachments/assets/240b26fc-4357-47f9-b891-4631f57f7f0d)

<p>This  differential amplifgier circuit has two resistors each of 1.81k,three voltage source,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=12.75um</p>
<p>Q point is(1.4v,0.6mA)</p>

#  Transient analysis
<p>Transient analysis of Input</p>  

![pckt3 tran in](https://github.com/user-attachments/assets/4206a789-5aaa-437c-95b6-78bc57df3bc4)
<p>Transient analysis of output</p> 

![pckt3 tran in](https://github.com/user-attachments/assets/e4d18705-01aa-4939-8482-23db2f61ff0d)
<p>Transient analysis of both input and output</p>

![pckt3 tran inout](https://github.com/user-attachments/assets/67d47bbb-c433-4c0d-80cc-2af59e8209c9)
<br>
<p>From the above figure we can clearly observe ,the 180 degree phase shift between input and output</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub></p>
<p>From graph we have v p-p voltages as</p>
<p>V<sub>in</sub>=1.34466-1.25634=0.08832</p>
<p>V<sub>out</sub>=1.41159-1.389675=0.021915</p>
<p>A<sub>v</sub>=V<sub>out</sub>/V<sub>in</sub>=0.012915/0.08831=0.2481 V/V</p>
<br>

# Ac analysis
<p>Ac analysis of the given circuit</p>

![pckt3 ac analysis](https://github.com/user-attachments/assets/9465edec-d5f1-4b33-9328-c758e252cf75)
<br>

![pckt3 bandwidth](https://github.com/user-attachments/assets/2c18f362-6c13-4201-b991-abb7a72c80e6)<br>
<p>Gain remains constant as their is no change in R<sub>d</sub>.From the above smulation the maximum frequency range is 17.203GHz and low frequency range is 100MHz.</p>
 <p>The bandwidth of this circuit is BW = f<sub>h</sub>-f<sub>l</sub></p>
 <p>BW= 17.203GHz-100mHz =17.203 GHz</p>

![pckt3 maximum gain](https://github.com/user-attachments/assets/0e8a7fda-f473-49c0-8bb4-ba4dc2c91e81)
<br>
<p>From the above figure we can note the maximum gain in db </p>
<p>A<sub>v</sub> in db=0.9db</p>
<br>

# Result
<p>The result of a differential amplifier is the amplified difference between the two input signals. The output voltage (V<sub>out</sub>) is calculated as:
V<sub>out</sub> = A<sub>d</sub> * (V<sub>+</sub> - V<sub>-</sub>)<br>
Where:
( A_d ) is the differential gain of the amplifier, which determines how much the difference between the inputs is amplified.<br>
( V<sub>+</sub>) is the voltage at the non-inverting input.<br>

( V<sub>-</sub>) is the voltage at the inverting input. <br>

The output is proportional to the difference between the non-inverting and inverting inputs. If the inputs are the same, the output is zero, as there is no difference to amplify.

Additionally, the amplifier ideally rejects any common-mode voltage that is present equally on both inputs. This is described by the common-mode rejection ratio (CMRR), which quantifies the amplifier's ability to reject common-mode signals and amplify only the differential signal. A high CMRR indicates the amplifier is very effective at rejecting unwanted common-mode noise.

In a practical scenario:
- If the difference between the inputs is small (e.g., millivolts), the output will be amplified according to the gain.
- If both inputs have the same voltage (i.e., no difference), the output will be zero.
  
This makes the differential amplifier particularly useful for weak signal amplification in the presence of noise, such as in instrumentation and communication systems.</p>
<br>

# Inference
<p>In the comparative analysis of the three differential amplifier circuits, the choice of tail current implementation significantly influences performance. The first circuit, utilizing a resistor R<sub>ss</sub>, exhibits sensitivity to power supply variations and transistor mismatches, leading to potential instability in the bias current and reduced common-mode rejection ratio. This is due to the resistor's limited ability to maintain a constant current under varying conditions. In contrast, the second circuit employs an ideal current source, ensuring a stable bias current that is largely unaffected by external fluctuations, thereby enhancing both stability and CMRR. The third circuit replaces R<sub>ss</sub> with an NMOS transistor configured as a current source with a gate voltage V<sub>b</sub></sub> of 0.76 V. This active current source provides improved performance over the resistor by offering higher output impedance, which contributes to better bias stability and CMRR. However, it may still be susceptible to variations due to transistor parameters and temperature changes. Overall, transitioning from a passive resistor to active current sources in differential amplifier designs leads to enhanced performance, with ideal current sources offering the most significant improvements. </p>













