# SeamCarving

## Description

This project involves the implementation of the Seam Carving algorithm and parallelization to enhance execution speed. Various parallelization optimizations have been applied to improve performance.

## Team Members

- Bùi Quang Bảo
- Hồ Hoàng Duy
- Lục Minh Bửu

## Timeline

December 2022 - January 2023

## Seam Carving Algorithm

The Seam Carving algorithm is used for resizing images, specifically reducing the width of the image by removing the least important pixels.

## Parallelizable Operations

1. Grayscale the image.
2. Calculate energy (via convolution).
3. Identify the least energy seam.
4. Remove the least important seam.

## Improvements

### Improvement 1

- Utilize CMEM instead of GMEM for constant variables.
- Reload reused variables from the previous execution to minimize copy operations between the host and device.

### Improvement 2

Overlap the copy input, grayscale, and convolution steps into n streams (where n is a parameter).

### See full report at SeamCarving.ipynb
