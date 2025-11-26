# Amplitude-Modulation

EXP NO: 1	GENERATION AND DETECTION OF AM

AIM:

To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.
Need for modulation is as follows:
•	Avoid mixing of signals
•	Reduction in antenna height
•	long distance communication
•	Multiplexing
•	Improve the quality of reception
•	Ease of radiation.
Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.
1)	Under modulation :	m<1, Em < Ec
2)	Critical modulation: m-1, Em = Ec
3)	Over modulation:	m>1, Em > Ec



Note: Keep all the switch faults in off position

Algorithm
1.	Define Parameters
First, define the parameters for your signals:
•	Carrier frequency (fc)
•	Modulating signal frequency (fm)
•	Sampling frequency (Fs)
•	Duration of the signal (T)


2.	Create a time vector based on the sampling frequency and duration.
 
3.	Create Modulating Signal
Define the modulating signal (message signal).

4.	Create Carrier Signal
Define the carrier signal.


5.	Perform Amplitude Modulation
Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).


6.	Plot the Signals
Visualize the modulating, carrier, and modulated signals.


7.	Demodulate the AM Signal
To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

8.	Plot the Demodulated Signal
Visualize the demodulated signal.


9.	Compare Signals
Compare the original modulating signal with the demodulated signal. PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Program

```

clc;
clear;
close;
Ac=15.6;
Am=7.8;
Fc=3900;
Fm=390;
Fs=40000;
t=0:1/Fs:2/Fm;
E1=Am*sin(2*%pi*Fm*t);
subplot(4,1,1);
plot(t,E1);
xlabel("Time(s");
ylabel("Amplitude");
title("Message Signal");
E2=Ac*sin(2*%pi*Fc*t);
subplot(4,1,2);
plot(t,E2);
xlabel("Time(s");
ylabel("Amplitude");
title("Carrier Signal");
E3=(Ac+Am*sin(2*%pi*Fm*t)).sin(2%pi*Fc*t);
subplot(4,1,3);
plot(t,E3);
xlabel("Time(s");
ylabel("Amplitude");
title("AM Signal");
demodulated_signal=abs(hilbert(E3))-Ac;
subplot(4,1,4);
plot(t,demodulated_signal);
xlabel("Time(s");
ylabel("Amplitude");
title("Demodulated Signal");
xgrid();

```
Output Waveform

<img width="805" height="401" alt="image" src="https://github.com/user-attachments/assets/32f9042f-792c-4dc7-bf58-6044b0e06c8b" />




TABULATION:

<img width="916" height="1012" alt="image" src="https://github.com/user-attachments/assets/d549c644-079a-4670-a6c5-f5442b69ee60" />

<img width="680" height="1031" alt="image" src="https://github.com/user-attachments/assets/63fe6740-0973-4707-8024-8b66b29e6b95" />


Calculation
1.	ma (Theory) = am/ac =
2.	ma(Practical) = (Emax-Emin)/(Emax+Emin) =


MODEL GRAPH

<img width="702" height="929" alt="image" src="https://github.com/user-attachments/assets/3572941b-f347-4554-b4bb-7b98f4d08608" />


 
 


RESULT:
<img width="682" height="330" alt="image" src="https://github.com/user-attachments/assets/b6874d79-e72b-4fa1-87c1-bf2c8fd80321" />


