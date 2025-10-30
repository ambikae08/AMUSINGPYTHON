# AM USING PYTHON
Aim
To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

Apparatus Required
Software: Python with NumPy and Matplotlib libraries

Hardware: Personal Computer

Theory
Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal.

The general form of an AM signal is:

<img width="368" height="266" alt="image" src="https://github.com/user-attachments/assets/9995f980-c5bd-400e-a8d6-eeb534c68466" />


Algorithm

Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
Generate Time Axis: Create a time vector for the signal duration.
Generate Message Signal: Define the message signal as a cosine wave.
Generate Carrier Signal: Define the carrier signal as a cosine wave.
Modulate Signal: Apply the AM formula to obtain the modulated signal.
Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Python Code

```
import numpy as np
import matplotlib.pyplot as plt

Am=2.4
Ac=4.8
fc=2270
fm=227
fs=22700
t=np.arange(0,2/fm,1/fs)

m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
eam=(Ac+Am*np.cos(2*np.pi*fm*t))*np.cos(2*np.pi*fc*t)

plt.subplot(3,1,1)
plt.plot(t,m)
plt.show()

plt.subplot(3,1,2)
plt.plot(t,c)
plt.show()

plt.subplot(3,1,3)
plt.plot(t,eam)
plt.show() 
```
Output

![WhatsApp Image 2025-10-30 at 08 24 24_66965528](https://github.com/user-attachments/assets/c6d8ffd7-7c6e-49fb-a69b-a072b451b555)

Manual Calculation

![WhatsApp Image 2025-10-28 at 22 35 23_08f80ca2](https://github.com/user-attachments/assets/2ac1f1be-0c7b-4703-83df-825d97a29563)


Result

The message signal, carrier signal, and amplitude modulated (AM) signal are displayed in separate plots. Thus, amplitude modulation is successfully implemented using NumPy and Matplotlib.
