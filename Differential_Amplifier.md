## Lic-lab
## Experiment-1
<p>Differential amplifier analysis</p><br>
<p>This experiment shows the ac,dc and transient analysis of Differential amplifier </p><br>
<p>Question : Design Differential amplifier for the following specifications vdd=2.5v ,vicm=1.3v ,vocm=1.4v, vp=0.5v. Perform Dc analysis, transient analysis, frequency response and extract the required parameters.</p><br>

## Abstract
<p> We need to design a differential amplifier with specific voltage and input signal requirements. The task involves performing four key analyses: DC Analysis to determine the operating point, Transient Analysis to observe how the amplifier responds to changing signals, Frequency Response to check its performance across different frequencies, and Parameter Extraction to gather important details like gain, bandwidth. We also need to find input swing and output swing.The goal is to ensure the amplifier works effectively within the given specifications.
</p>

##Theory
<p> A differential amplifier is a type of electronic amplifier that amplifies the difference between two input signals. It has two inputs: a non-inverting input and an inverting input. The amplifier increases the voltage difference between these inputs while rejecting any voltage common to both, called the common-mode voltage. This makes it highly effective for applications where the signal needs to be isolated from noise or interference. Differential amplifiers are widely used in signal processing, instrumentation, and communication systems due to their ability to amplify weak signals while rejecting noise.
</p>

# circuit 1
![image](https://github.com/user-attachments/assets/f7b17338-032b-4b6e-b4bb-fea5e98ce8d8)
<p>This circuit consists of two nmos transistors ,3 resistors 2 voltage sources and vdd</p>
<p>mosfets of length 180nm</p>
<p>mosfets of width 1um</p>
<p>rd of 1.8k ohm</p>
<p>rss of 416.66 ohm</p>
<p>vdd of 2.5v</p>
<p>vicm of each 1.3v</p>

#  Dc analysis
<p>The DC analysis of a differential amplifier involves determining the biasing conditions of the circuit when no input signal is applied (i.e., with a constant DC voltage). This analysis helps set the operating point of the transistors, ensuring they work in their active region. Key parameters like the quiescent currents, voltages across components, and the overall stability of the circuit are determined. DC analysis is essential for setting the proper biasing to ensure the amplifier functions correctly when signals are later applied.</p>

![image](https://github.com/user-attachments/assets/b6b21f34-1b04-48b2-9755-087bc9031496)
![image](https://github.com/user-attachments/assets/fae7b6ca-9762-4fc1-ba98-4a00b1988f7a)

<p>This  differential amplifgier circuit has two resistors each of 1.8k,two voltage source of 1.3v,vdd=2.5v</p>
<p>Mosfet length= 180nm</p>
<p>width=7.99um</p>
<p>Q point is(1.4v,0.6mA)</p>

# Transient analysis
<p>Transient analysis of a differential amplifier studies how the circuit responds to changes in the input signal over time. It simulates the amplifier’s behavior when the input voltage suddenly changes, such as when a pulse or step input is applied. This analysis helps determine how quickly the amplifier can respond, including how long it takes to reach a stable output, known as rise time, fall time, and settling time. It ensures the amplifier can accurately amplify signals without distortion or delays when dealing with real-time, rapidly changing inputs.</p>

# Ac analysis
<p> AC analysis of a differential amplifier looks at how the amplifier responds to changing input signals, like alternating current (AC) signals. It helps determine how much the amplifier amplifies the input signal (gain) and how well it performs across different frequencies. This analysis shows the frequency response, such as the bandwidth and cutoff points, which indicates how effectively the amplifier handles high or low-frequency signals. Essentially, AC analysis helps ensure the amplifier works well with real-world, time-varying signals.</p>

# Input swing
<p>The input swing of a differential amplifier refers to the range of input voltages over which the amplifier can operate correctly without distortion. It represents the minimum and maximum input voltages that can be applied to the amplifier's inputs while still allowing it to produce an accurate output. If the input signal goes beyond this range, the amplifier may enter saturation or cutoff, causing the output to be distorted or clipped. The input swing is important for ensuring the amplifier can handle varying input signals without losing performance.</p>
 
