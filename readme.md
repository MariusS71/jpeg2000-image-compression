# JPEG 2000 Image Compression

This project explores the implementation of the **JPEG 2000** standard, focusing on efficient image compression using wavelet transforms, quantization, and adaptive arithmetic encoding. The project demonstrates how JPEG 2000 improves upon traditional JPEG by offering better compression ratios and higher image quality.

## 📊 Project Overview
- **Objective**: Develop an application that implements JPEG 2000 compression and decompression for color images, focusing on optimizing storage and transmission efficiency.
- **Technologies Used**: Python, scikit-image, PyWavelets.
- **Team Members**: Marius-Andrei Saioc, Maria-Cristina Sima.

##  Methodology
1. **Preprocessing**:
   - Conversion of images from **RGB to YCbCr** color space for efficient compression.
   - Normalization of pixel values to optimize wavelet processing.

2. **Discrete Wavelet Transform (DWT)**:
   - Utilizes the **'bior4.4'** filter to decompose images into sub-bands (LL, LH, HL, HH).
   - The first level of decomposition is used to extract significant features.

3. **Quantization**:
   - Implements a **uniform quantizer with deadzone** to reduce the bit-rate while maintaining visual quality.
   - Focuses on compressing low-frequency components (LL) while preserving important details.

4. **Entropy Encoding**:
   - Uses **adaptive binary arithmetic encoding** to efficiently compress quantized coefficients into a compact bitstream.

5. **Decompression**:
   - Includes inverse quantization, inverse DWT, and conversion back to RGB color space.
   - Reconstructs the image while retaining high visual fidelity.

##  Key Features
- Implementation of JPEG 2000 compression using Python libraries.
- Supports color images with lossy compression for optimized storage.
- Achieves high **PSNR** and low **MSE** compared to standard JPEG.

##  Results
- **PSNR**: JPEG 2000 achieved **37.73 dB**, compared to **33.21 dB** for JPEG.
- **MSE**: JPEG 2000 had an **MSE of 10.96**, significantly lower than JPEG's **31.06**.
- **Standard Deviation of Difference**: JPEG 2000 showed better consistency with a lower deviation compared to JPEG.

##  Conclusion
The project successfully implemented the core functionalities of JPEG 2000 for color image compression, demonstrating significant improvements over traditional JPEG in terms of quality and efficiency. Future improvements include optimizing quantization and extending support for higher levels of wavelet decomposition.


