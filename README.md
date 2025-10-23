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


Am=6.7
fm=528
fs=52800
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

Ac=13.4
fc=5280
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

am=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,am)
plt.show()



```

## Output Waveform

<img width="700" height="517" alt="image" src="https://github.com/user-attachments/assets/0c39268f-2f31-4664-bd50-9dc53588e57b" />



## Tabular Column

![WhatsApp Image 2025-10-23 at 22 57 23_e218efde](https://github.com/user-attachments/assets/31b983e3-88f2-4f25-a11f-ad42c17f25c4)


## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
