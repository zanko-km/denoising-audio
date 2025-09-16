# Audio Denoising Using Fourier Transform and Band-Pass Filter

## Project Overview

In this project, we **analyzed and cleaned a noisy voice recording**.  
We examined the frequency variations in the audio using **Fourier Transform** and applied a **band-pass filter** to remove unwanted noise.  

Since the noise frequency does not overlap with the voice frequency, the filtering process is straightforward. Otherwise, more advanced and complex denoising methods would have been required.

## Methodology

### Fourier Transform
The **Fourier Transform** is a mathematical technique that transforms a time-domain signal into its **frequency-domain representation**.  
- It allows us to see which frequencies are present in the audio.  
- By analyzing the frequency spectrum, we can identify and isolate noise from the desired signal.

### Band-Pass Filter
A **band-pass filter** allows frequencies within a specific range to pass through while **blocking frequencies outside that range**.  
- In this project, we set the filter to pass the voice frequency band and remove frequencies corresponding to noise.  
- Since the noise frequency is separate from the voice frequency, a simple band-pass filter is sufficient.  

### Workflow

1. **Load the audio**  
   - Use Python libraries such as `librosa` or `scipy` to read the noisy voice file.

2. **Fourier Analysis**  
   - Apply Fourier Transform to convert the signal to the frequency domain.  
   - Visualize the frequency spectrum to identify the noise components.

3. **Filtering**  
   - Apply a band-pass filter to remove unwanted noise.  

4. **Reconstruct Audio**  
   - Convert the filtered frequency-domain signal back to the time domain.  
   - Save the denoised audio file.

5. **Evaluation**  
   - Compare the original and denoised audio qualitatively and, optionally, quantitatively using **Signal-to-Noise Ratio (SNR)**.
