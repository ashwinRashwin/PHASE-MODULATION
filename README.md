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
Am=3.05;
Ac=5.645;
fm=579;
fc=5790;
fs=57900;
B=4.04;
Kp=B;
t=0:1/fs:2/fm;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos((2*3.14*fc*t)+(B*sin(2*3.14*fm*t)));
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos((2*3.14*fc*t)+(Kp*cos(2*3.14*fm*t)));
subplot(4,1,4);
plot(t,epm);

~~~
OUTPUT WAVEFORM

<img width="1917" height="883" alt="image" src="https://github.com/user-attachments/assets/940a05af-e9e6-4d11-8f72-c7d68bf0ff90" />


TABULATION

<img width="846" height="1447" alt="WhatsApp Image 2026-09-25 at 12 10 16 PM" src="https://github.com/user-attachments/assets/865b9f2a-0d93-44c1-8cec-ac50ac513a82" />


CALCULATION

<img width="975" height="1396" alt="WhatsApp Image 2026-09-25 at 1 07 16 PM" src="https://github.com/user-attachments/assets/bf76d416-6ac1-4e69-82a3-5c01b564b5ff" />

RESULT
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.

