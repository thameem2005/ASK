## AIM
To perform Amplitude Shift Keying{ASK} using Python
## APPARATUS REQUIRED:
Python 3.x
## PROGRAM
```
import numpy as np
import matplotlib.pyplot as plt

# Parameters
fs = 1000  # Sampling frequency
fc = 100   # Carrier frequency
bit_rate = 10  # Bit rate
t = np.arange(0, 1, 1/fs)  # Time vector

# Generating Random Binary Data
data = np.random.randint(0, 2, bit_rate)
bit_duration = 1 / bit_rate
bit_t = np.linspace(0, bit_duration, int(fs / bit_rate), endpoint=False)
signal = np.concatenate([np.ones_like(bit_t) * bit for bit in data])

# Carrier Signal
carrier = np.sin(2 * np.pi * fc * np.linspace(0, 1, len(signal), endpoint=False))

# ASK Modulation
ask_signal = signal * carrier

# Plot Signals
plt.figure(figsize=(12, 6))

plt.subplot(3, 1, 1)
plt.step(np.linspace(0, 1, len(signal)), signal, where='mid', label="Binary Data")
plt.legend()
plt.grid(True)

plt.subplot(3, 1, 2)
plt.plot(np.linspace(0, 1, len(carrier)), carrier, label="Carrier Signal")
plt.legend()
plt.grid(True)

plt.subplot(3, 1, 3)
plt.plot(np.linspace(0, 1, len(ask_signal)), ask_signal, label="ASK Modulated Signal")
plt.legend()
plt.grid(True)

plt.show()
```
## PROGRAM WAVEFRONT
![image](https://github.com/user-attachments/assets/2e925df8-9c0c-47b9-b155-065b60817cf7)

## GRAPH
![WhatsApp Image 2025-04-15 at 20 33 47_9f566fb5](https://github.com/user-attachments/assets/4db3ca85-6f41-4d47-a38b-d1954f331db8)
## RESULT
THUS THE ASK (Amplitude Shift Keying) IS PERFORMED USING PYTHON
