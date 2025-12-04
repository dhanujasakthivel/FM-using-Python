# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 3.7
Ac = 7.4
fm = 467
fc = 4670
fs = 46700
b = 2.66
t = np.arange(0,2/fm,1/fs)
m = Am * np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c = Ac * np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
mod = Ac * np.cos(2*np.pi*fc*t + b * np.sin(2*np.pi*fm*t))
plt.subplot(3,1,3)
plt.plot(t,mod)
```
Output Waveform

![WhatsApp Image 2025-11-25 at 10 39 35 PM](https://github.com/user-attachments/assets/f58dc6ca-e618-4fb6-a922-98505c601aff)

Tabular Column

![WhatsApp Image 2025-12-04 at 3 39 08 PM](https://github.com/user-attachments/assets/682581c2-0bbb-40fc-ad22-04e1b1c3d7bc)


Calculation

![WhatsApp Image 2025-11-25 at 10 39 35 PM (1)](https://github.com/user-attachments/assets/eedd4c39-c700-4a10-a015-72dd535c59d6)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
