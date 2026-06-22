# Autocorrelation

**Aim**:

Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

**Equipments Needed**:


Computer with Intel i3 processor (or higher) Scilab software

**Theory:**


The Wiener–Khinchin theorem states that:

The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

<img width="1062" height="301" alt="image" src="https://github.com/user-attachments/assets/606d467f-5a27-4584-a1fe-5b78109f05fa" />



This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

**Algorithm:**
Load or Define the Signal: Input your time-domain signal. Compute Autocorrelation: Calculate the autocorrelation function of the signal. Compute Power Spectral Density (PSD): Estimate the PSD using either: Fourier Transform of the autocorrelation function, or Methods like Welch’s periodogram. Plot Results: Visualize both the autocorrelation function and PSD.

**Procedure:**
Refer to the algorithm and write the code for the experiment. Open Scilab on your system. Type your code in a new editor. Save the file. Execute the code. If any errors occur, debug and re-run the program. Verify the generated waveform using tabulation and model waveform comparison.

**Program (Scilab Code):**
```
clc;
clear all;
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


**Output:**
<img width="1918" height="1198" alt="image" src="https://github.com/user-attachments/assets/2a83d7b9-a116-4bd6-88c7-69aec8289139" />

**signed output**:
<img width="1270" height="738" alt="image" src="https://github.com/user-attachments/assets/a7f0d749-6915-4af8-b613-84caafc31291" />


**Result:**
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
