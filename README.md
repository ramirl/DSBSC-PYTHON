AIM:

To write a program to perform DSBSC modulation and demodulation using PYTHON and study its spectral characteristics

EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open PYTHON COLLAB
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Program
```
import numpy as np
import matplotlib.pyplot as plt

# Parameters
Am = 4.4      # Message amplitude
Ac = 9    # Carrier amplitude
fm = 352      # Message frequency (Hz)
fc = 3520     # Carrier frequency (Hz)
fs = 352000   # Sampling frequency (Hz)

# Time vector
t = np.arange(0, 2/fm, 1/fs)

# Message signal
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.title("Message Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

# Carrier signal
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.title("Carrier Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

# DSB-SC Modulated Signal
s = m * c
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.title("DSB-SC Modulated Signal")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")

# Layout and show
plt.tight_layout()
plt.show()
```
Output Graph

![WhatsApp Image 2025-11-16 at 19 49 08_8e0dfdcb](https://github.com/user-attachments/assets/2f609325-e869-45a2-982d-1f7c7cc9ef28)


Tablular Column:

![WhatsApp Image 2025-12-03 at 20 16 14_d435ed76](https://github.com/user-attachments/assets/f1bca4e2-414e-44a7-94e4-d5d0a5c1c6af)


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

