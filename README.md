# auto-correlation-and-PSD-

AIM:
Aim: To simulate AUTO CORRELATION AND PSD of signal in SCILAB and verify Khinchin relation.
EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:


Note: Keep all the switch faults in off position

Algorithm
1. Start the program.
2. Generate a sinusoidal signal.
3. Compute and plot its autocorrelation sequence.
4. Find the FFT of the autocorrelation.
5. Compute the FFT of the signal.
6. Calculate the Power Spectral Density using |FFT(x)|².
7. Plot the obtained spectra.
8. Verify that the Fourier Transform of the autocorrelation equals the PSD.
9. Stop the program.
Program
```
clc
clear all

t=0:0.01:2*%pi;
x=sin(2*t);

subplot(3,2,1);
plot(x);

au=xcorr(x,x);
subplot(3,2,2);
plot(au);

v=fft(au);
subplot(3,2,3);
plot(abs(v));

fw=fft(x);
subplot(3,2,4);
plot(fw);

fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```
MODEL GRAPH
 <img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/55326c5b-7dd5-4873-aaf6-d219bb7c4420" />
 TABULATION:
<img width="637" height="332" alt="image" src="https://github.com/user-attachments/assets/7ff79056-9cf7-4ff0-a385-703060457972" />
Calculation
<img width="648" height="362" alt="image" src="https://github.com/user-attachments/assets/07db08ba-635e-410e-914a-efc758fa6b82" />

Output Waveform
<img width="760" height="580" alt="image" src="https://github.com/user-attachments/assets/3efbd926-dbb4-4692-9040-b72d6a7faf32" />

RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
