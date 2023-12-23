
Read and Preprocess Image:
Load an image (npimage5.jpg in this case).
Convert the image to grayscale.
Apply bilateral filter and Canny edge detection to enhance edges.

Contour Detection:
Find contours in the processed image.
Sort the contours by area in descending order and keep the top 15.

License Plate Location:
Iterate through the sorted contours and find the contour with four vertices (a rectangle), which is likely the license plate.

Masking and Cropping:
Create a mask using the contour of the license plate.
Apply the mask to the original image to extract the license plate region.
Crop the license plate region.

Text Recognition:
Use EasyOCR to perform optical character recognition (OCR) on the cropped license plate region.

Display Results:
Display the intermediate and final results using Matplotlib.
