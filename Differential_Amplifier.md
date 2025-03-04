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



 
