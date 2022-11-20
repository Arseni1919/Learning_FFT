# Learning FFT

Here’s some code that generates a sine wave:

```python

import numpy as np
from matplotlib import pyplot as plt

SAMPLE_RATE = 44100  # Hertz
DURATION = 5  # Seconds

def generate_sine_wave(freq, sample_rate, duration):
    x = np.linspace(0, duration, sample_rate * duration, endpoint=False)
    frequencies = x * freq
    # 2pi because np.sin takes radians
    y = np.sin((2 * np.pi) * frequencies)
    return x, y

# Generate a 2 hertz sine wave that lasts for 5 seconds
x, y = generate_sine_wave(2, SAMPLE_RATE, DURATION)
plt.plot(x, y)
plt.show()
```

```python
yf = fft(normalized_tone)
xf = fftfreq(N, 1 / SAMPLE_RATE)
```
The code calls two very important functions:

1. fft() calculates the transform itself.

1. fftfreq() calculates the frequencies in the center of each bin in the output of fft(). Without this, there would be no way to plot the x-axis on your frequency spectrum.


## Credits

- [realpython | fft](https://realpython.com/python-scipy-fft/)
- [youtube | But what is the Fourier Transform? A visual introduction.](https://www.youtube.com/watch?v=spUNpyF58BY&ab_channel=3Blue1Brown)
- []()
- []()
- []()