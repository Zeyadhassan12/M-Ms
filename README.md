# M-Ms
identifying and visualizing circles and blue-colored circles using OpenCV.

This script processes a set of .png images in a specified directory, identifying and visualizing circles and blue-colored circles using OpenCV. Here’s a summary of each major section:

Script Overview
Directory and Image Loading:
The directory containing .png images is specified, and all files with the .png extension are retrieved.
Image Preprocessing:
Each image is loaded in a loop.
The image is converted to grayscale, and a mask is created to isolate blue regions based on predefined HSV boundaries.
Blue Region Masking:
The code applies a color mask to the image to isolate regions that are blue.
The blue regions are processed to grayscale, and a median blur is applied to reduce noise.
Circle Detection:
All Circles: A HoughCircles function is applied on the original grayscale image to detect circles of any color.
Blue Circles: Another HoughCircles function is applied specifically on the blue regions (after blurring) to detect circles within the masked blue area.
Each detected circle is visualized with different colors: green for all circles and red for blue circles.
Result Display:
For each image, the total circles and total blue circles detected are printed, and the image with detected circles is displayed.
Improvements
HSV for Blue Mask: Adjusting the blue mask to the HSV color space (instead of BGR) may improve detection accuracy, especially if lighting conditions vary.
Circle Count Accumulation: To get a summary of total circles across all images, use accumulators (total_circles and total_blue_circles) outside the loop and update these with each image’s counts.


