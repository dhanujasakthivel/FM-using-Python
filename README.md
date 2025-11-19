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
Am=3.7
Fm=467
Ac=7.4
Fc=4670
Fs=46700
t=np.arange(0,2/Fm,1/Fs)
m=Am*np.cos(2*3.14*Fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*Fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=Ac*np.cos((2*3.14*Fc*t)+(2.55*np.sin(2*3.14*Fm*t)))
plt.subplot(3,1,3)
plt.plot(t,s)
```

Output Waveform
<img width="562" height="426" alt="image" src="https://github.com/user-attachments/assets/781515e9-f1e4-4b08-a1b1-fc179d47f2bc" />


Tabular Column

![WhatsApp Image 2025-11-19 at 7 53 17 AM](https://github.com/user-attachments/assets/73c03515-8c0c-455c-8db2-f6e18144d7ba)


Calculation

![WhatsApp Image 2025-11-19 at 7 52 41 AM](https://github.com/user-attachments/assets/65fffb7d-539e-4626-a31c-92c9744d5a9e)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
