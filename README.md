# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
```
Am = 11.8;
Fm = 560;
B  = 6.1;
Ac = 23.6;
Fc = 5600;
Fs = 99000;
T  = 0:1/Fs:2/Fm;
em = Am * cos(2*%pi*Fm*T);
subplot(3,1,1);
plot(T, em);
xtitle("Message Signal");
xgrid();
ec = Ac * cos(2*%pi*Fc*T);
subplot(3,1,2);
plot(T, ec);
xtitle("Carrier Signal");
xgrid();
efm = Ac * cos( (2*%pi*Fc*T) + (B * sin(2*%pi*Fm*T)) );
subplot(3,1,3);
plot(T, efm);
xtitle("FM Signal");
xgrid();
```


Output Waveform

<img width="1912" height="1135" alt="image" src="https://github.com/user-attachments/assets/80a40c91-cf9a-4071-b75f-199165187535" />

Tabulation

![WhatsApp Image 2025-11-16 at 15 16 11](https://github.com/user-attachments/assets/175cb08a-8f99-43dd-b619-d75711e0ba33)

Calculation

![WhatsApp Image 2025-11-16 at 15 16 11 (1)](https://github.com/user-attachments/assets/b006e4fc-452d-4e92-a370-1fde88554d8a)

Frequency Deviation Practical 
```
fc - fmin
= 5600 - 2408.9
= 3191.1 Hz
```
Modulation Index Practical = 6.1

Modulation Index Theoretical	= 3191.1/560 = 5.7



RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


