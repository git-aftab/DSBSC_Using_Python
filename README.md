#DSBSC USING PYTHON

<h2>EX NO: 6 DSB-SC-AM MODULATOR AND DEMODULATOR USING PYTHON</h2>

<h3>AIM</h3>
To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics.

<h3>EQUIPMENTS REQUIRED</h3>

• Computer with i3 Processor • CO LAB.

Note: Keep all the switch faults in off position

<h3>Algorithm:</h3>

1. Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
2. Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3. DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4. DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5. Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE
• Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

<h3>Model Waveform</h3>
<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

#program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 6.4     
Ac = 12.8   
fm = 590   
fc = 5900   
fs = 59000   
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```
<h3>Output Graph</h3>
<img width="1536" height="898" alt="DSBSC_PY" src="https://github.com/user-attachments/assets/6011556d-87f9-4a53-80d2-dd03a0c313ae" />



<h3>Result:</h3>
Thus the DSB-SC-AM Modulation and Demodulation using python is generated.
