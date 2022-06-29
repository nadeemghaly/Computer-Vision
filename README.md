# Computer-Vision
Computer Vision processing done in Python

## Assignment 1
Color quantization was done in the follow sequeunce:
  1. CalculateColorMap: here we find all the colors in the image and the total number of pixels that use this color
  2. QuantizationLevels: we give this function d (delta) and for for each color, we should have a quantized color (C) that covers this color ( C-D <= pixel <= C+D)
  3. AdjustIndex: Adjust index of each pixel according to its color to match the index from the newly quantized colors
  4. ReverseColorMap: flip the keys and values for the dictionary that contains quantized images
  5. ColorMapToImage: match color of each index from step 4

## Assignment 2:
Equalizing image was done on a Black and White image in the follow sequence:
  1. CalculateHistogram: where we calcaulte the histogram of each grey level 0-255
  2. CalculateCumulativeHistogram: where we convert the previous histogram to a cumalative one
  3. CalculateEqualizedHistogram: we equalite the cumalative histogram calculated in 2
  4. CalculateEqualizedImage: where we replace each pixel in the original image with its new equalized grey scale level

Optimal Segmenting on the image was done as follows:
  1. GetThreshhold: where we calculate the average of the grey levels, then assign the average to this then recalculate again till the code converges
  2. SegmentOptimalThresholding: we either assign 0 or 255 depending if the grey level of the pixel is over or under the treshhold

## Assignment 3:
Here we apply Image Segmentation using K-Means clustering on colored and BW images which is done by:
  1. Finding the closest center to each pixel and assign it to this center
  2. Calculate new centers by dividing the sum of the pixels assigned to each cluster and dividing by their number
  3. If centers didnot change from last iteration, this means that the code converged and the centers are chosen perfectly
  4. change the value of each pixel with the center closest to it
