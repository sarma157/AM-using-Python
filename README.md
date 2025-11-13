# AM-using-Python

## Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
```
import numpy as np
import matplotlib.pyplot as plt


Am=6.9
fm=542
fs=54200
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

Ac=13.8
fc=5420
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

am=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,am)
plt.show()



```

## Output Waveform

<img width="713" height="556" alt="image" src="https://github.com/user-attachments/assets/0d75530d-ae11-41a6-9110-f3923a80ea37" />




## Tabular Column

![WhatsApp Image 2025-11-13 at 12 52 29_2a466910](https://github.com/user-attachments/assets/c249b90f-ed67-43be-b428-d686c3d590e5)



## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
