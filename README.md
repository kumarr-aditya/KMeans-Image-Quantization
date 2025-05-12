# Image Compression Using K-Means Clustering

This project demonstrates how to compress images by reducing their color space using the K-Means clustering algorithm. By clustering similar colors and representing them with their respective cluster centroids, we can achieve significant compression while preserving the visual quality of the image.

## Overview

In a typical 24-bit color image, each pixel is represented by three 8-bit values corresponding to the Red, Green, and Blue channels. This allows for over 16 million possible color combinations. However, many images contain a limited set of dominant colors. By applying K-Means clustering to the pixel colors, we can reduce the number of unique colors in the image to a predefined number $k$, effectively compressing the image.

The process involves:

1. Reshaping the image into a two-dimensional array where each row represents a pixel's RGB values.
2. Applying the K-Means algorithm to cluster the pixel colors into $k$ clusters.
3. Replacing each pixel's color with the nearest cluster centroid color.
4. Reshaping the array back to the original image dimensions to obtain the compressed image.

## Features

* Compress images by reducing the number of unique colors.
* Adjustable number of clusters $k$ to control the compression level.
* Supports common image formats like PNG and JPEG.
* Visual comparison between the original and compressed images.

## Requirements

* scikit-learn
* pandas
* matplotlib
* pillow
* pypng

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/kumarr-aditya/KMeans-Image-Quantization
   cd KMeans-Image-Quantization
   ```


2\. Install the required packages:

```bash
pip install -r requirements.txt
```


## Example

Original Image:
![Original Image](https://github.com/kumarr-aditya/KMeans-Image-Quantization/blob/main/test_pictures/image_portrait.png)

Compressed Image with $k=32$:
![Compressed Image](https://github.com/kumarr-aditya/KMeans-Image-Quantization/blob/main/compressed_outputs/image_portrait.png)

## Notes

* Choosing a higher value of $k$ retains more color details but results in less compression. Conversely, a lower $k$ increases compression but may reduce image quality.
* For best results, use images in PNG format to avoid artifacts from prior compression.
