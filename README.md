# PHASE-MODULATION
EXP - 05

AIM

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries.

APPARATUS REQUIRED
Software: Scilab Hardware: Personal Computer

THEORY
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

The general form of a PM signal can be represented as:

<img width="816" height="464" alt="image" src="https://github.com/user-attachments/assets/304524c7-3a06-492d-9221-aebdaf208c13" />

ALGORITHM

Initialize Parameters: Set the values of carrier amplitude, carrier frequency, message frequency, sampling frequency and phase deviation sensitivity.

Generate Time Axis: Create a time vector for the required signal duration using the sampling frequency.

Generate Message Signal: Generate the message signal as a cosine wave.

Generate Carrier Signal: Generate the carrier signal using the carrier amplitude and carrier frequency.

Generate PM Signal: Apply the phase modulation equation using the message and carrier signals to obtain the phase-modulated signal.

Plot the Signals: Plot the message signal, carrier signal and phase-modulated signal using Scilab plotting commands.

Display the Result: Observe the phase variation of the carrier signal according to the message signal.

PROGRAM
~~~
clc;
clear;

t = 0:0.01:2*3.14;
x = sin(6*t);

subplot(3,2,1);
plot(x);

au = xcorr(x,x);

subplot(3,2,2);
plot(au);

v = fft(au);

subplot(3,2,3);
plot(abs(v));

fw = fft(x);

subplot(3,2,4);
plot(real(fw), imag(fw));

fw2 = (abs(fw)).^2;

subplot(3,2,5);
plot(fw2);
~~~
TABULATION

<img width="1599" height="899" alt="WhatsApp Image 2026-09-02 at 22 18 50" src="https://github.com/user-attachments/assets/4e256998-b68a-4de4-9d4f-789bd16c4888" />

CALCULATION

<img width="1600" height="1402" alt="WhatsApp Image 2026-09-02 at 22 19 45" src="https://github.com/user-attachments/assets/b25eba04-b51d-44a5-9a02-9ff31056cc71" />
<img width="899" height="1599" alt="WhatsApp Image 2026-09-02 at 22 19 29" src="https://github.com/user-attachments/assets/f86419a2-498b-4494-8875-f2156f562d1b" />

RESULT
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.

