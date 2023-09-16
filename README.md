# tugas-sinyal
# Result Tugas 1 PSO
# A. IPython Console from Spyder showing Name and NRP
Nama: Julio Maulana Bagus Penag
NRP: 5009211144
![vffk0qrt](https://github.com/JulioMaulana/tugas-sinyal/assets/144867340/685bdce9-1187-4845-8e34-700206325db5)
# B. Result and Script on Spyder
![Screenshot (103)](https://github.com/JulioMaulana/tugas-sinyal/assets/144867340/72f7af02-161d-4643-ae67-c8a4e4ed371b)
[Uploading Result Rimport numpy as np
import matplotlib.pyplot as plt
from scipy.signal import convolve

# Create a time vector
t = np.linspace(0, 1, 1000, endpoint=False)

# Create a simple signal (e.g., a sine wave)
signal = np.sin(2 * np.pi * 5 * t)

# Add noise to the signal
noise = np.random.normal(0, 0.5, t.shape)
noisy_signal = signal + noise

# Define a moving-average filter kernel
window_size = 10
kernel = np.ones(window_size) / window_size

# Apply the filter using convolution
filtered_signal = convolve(noisy_signal, kernel, mode='same')

# Plot the original signal, noisy signal, and filtered signal
plt.figure(figsize=(12, 6))
plt.plot(t, signal, label='Original Signal', linewidth=2)
plt.plot(t, noisy_signal, label='Noisy Signal', alpha=0.7)
plt.plot(t, filtered_signal, label='Filtered Signal', linewidth=2)
plt.legend()
plt.title('Signal Filtering')
plt.xlabel('Time')
plt.ylabel('Amplitude')
plt.grid(True)
plt.show()

# Perform FFT on the noisy signal
fft_result = np.fft.fft(noisy_signal)
frequencies = np.fft.fftfreq(len(t), t[1] - t[0])

# Plot the magnitude of the FFT result
plt.figure(figsize=(12, 6))
plt.plot(frequencies, np.abs(fft_result))
plt.title('Fast Fourier Transform (FFT)')
plt.xlabel('Frequency (Hz)')
plt.ylabel('Magnitude')
plt.grid(True)
plt.show()

# Create two signals for convolution
signal1 = np.array([1, 2, 3, 4, 5])
signal2 = np.array([0.1, 0.2, 0.3])

# Perform convolution
conv_result = np.convolve(signal1, signal2, mode='valid')

# Plot the convolution result
plt.figure(figsize=(8, 4))
plt.stem(conv_result)
plt.title('Convolution')
plt.xlabel('Sample Index')
plt.ylabel('Amplitude')
plt.grid(True)
plt.show()
estrictions.py…]()

# C. Last Commit Logs
![Screenshot (101)](https://github.com/JulioMaulana/tugas-sinyal/assets/144867340/d5c986c5-b792-4646-ad98-d490e9d38ebd)
