# Docment-Scanner-using-openCV-and-python
A simple picture scanner which accepts documents in the form of pictures, and scans them to form a proper shaped pdf document.
Here, many basic openCV functions have been used to detect and draw contours, edges and so on. There are 3 basic steps in this project-
1. Detect edges.
2. Detect contours and extract the cotours having 4 edges.
3. Perform 4 point transform on the original document, using the extracted contour shape metrics.

## Please make sure that the transform.py file is in a folder named transform.


# Check your work output by printing these lines after my indicated step-over sign

1st step:
'''print("STEP 1: Edge Detection")
cv2.imshow("Image", image)
cv2.imshow("Edged", edged)
cv2.waitKey(0)
cv2.destroyAllWindows()'''

2nd step:

'''print("STEP 2: Find contours of paper")
cv2.drawContours(image, [screenCnt], -1, (0, 255, 0), 2)
cv2.imshow("Outline", image)
cv2.waitKey(0)
cv2.destroyAllWindows()'''

3rd step:

print statements are present in code

To run the code, type- 
### $python3 document_scanner.py --images receipt.jpg

The transform folder contains the transform.py function, which transforms the original picture into the reshaped pdf type document,
and returns the transformed image. The image is then subjected to local thresholding to give the black and white effect.
To know more about thresholding, visit here- https://scikit-image.org/docs/0.13.x/auto_examples/xx_applications/plot_thresholding.html

Finally, using imshow the thresholded image is displayed.
