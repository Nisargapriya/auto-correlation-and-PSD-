# auto-correlation-and-PSD-

AIM:
Aim: To simulate AUTO CORRELATION AND PSD of signal in SCILAB and verify Khinchin relation.
EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

THEORY:


Autocorrelation is a mathematical operation used to measure the similarity between a signal and its time-shifted version. It indicates how closely a signal matches with itself at different time delays.

For a periodic signal, the autocorrelation function is also periodic and attains its maximum value at zero time shift. Autocorrelation is widely used in signal processing for detecting periodicity, estimating signal power, and analyzing random signals.

The autocorrelation function of a signal x(t) is given by:

Rxx(τ) = ∫ x(t) x(t + τ) dt

where,

Rxx(τ) = Autocorrelation function
x(t) = Original signal
τ = Time delay (lag)

According to the Wiener–Khinchin theorem, the Fourier Transform of the autocorrelation function gives the Power Spectral Density (PSD) of the signal.

PSD = F{Rxx(τ)}

Autocorrelation helps in determining the degree of similarity of a signal with itself and is extensively used in communication and digital signal processing applications.

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
Output Waveform
<img width="1192" height="736" alt="image" src="https://github.com/user-attachments/assets/cdc59b4b-257c-4594-b29f-4780a0a03b32" />


RESULT:
Thus, the autocorrelation of the given signal is obtained and its corresponding Power Spectral Density (PSD) is verified using the Wiener–Khinchin theorem.
