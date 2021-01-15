# Keypoint Description and Matching

## Problem 1: Keypoint Detection
Compute the Harris corner detector using the following steps

### (a)
Compute the x and y derivatives on the image.
### (b)
Compute the covariance matrix H of the image derivatives. Typically, when you compute the covariance matrix you compute the sum of I x 2 , I y 2 and I x I y over a window or small area of the image. To obtain a smooth result for better detection of corners, use a Gaussian weighted window.
### (c)
Compute the Harris response using det(H)/trace(H)
### (d)
Find peaks in the response that are above the threshold, and store the interest point locations.
### (e)
Open ”Boxes.png” and compute the Harris corners. Save an image ”1a.png” showing the Harris response on ”Boxes.png”.
### (f)
Compute the Harris corner detector for images ”Rainier1.png” and ”Rainier2.png”. Save the images ”1b.png” and ”1c.png” of the detected corners.

## Problem 2: Keypoint Matching
Matching the interest points between two images.
### (a)
Compute the descriptors for each interest point. (You can use any descriptor. For example ORB)
### (b)
For each interest point in image 1, find its best match in image 2. The best match is defined as the interest point with the closest descriptor (SSD or ratio test).
### (c)
Add the pair of matching points to the list of matches.
### (d)
Display the matches. You should see many correct and incorrect matches.
### (e)
Compute the Harris corner detector and find matches for images ”Rainier1.png” and ”Rainier2.png”. Save the image ”2a.png” showing the image with the found matches.
### (f)
Compute the Harris corner detector, find matches and run RANSAC for images ”Rainier1.png” and ”Rainier2.png”. Save the image ”2b.png” of the found matches. You should only see correct matches, i.e. , all the incorrect matches from the previous step should be removed. If you see all or some incorrect matches try running RANSAC with a larger number of iterations. You may try tuning the other parameters as well.

## Problem 3: Image Stitching
Stitch the images together using the computed homography. Implement the function stitch(image1,image2, hom, homInv, stitchedImage). Follow these steps:
### (a)
Compute the size of ”stitchedImage. ” To do this project the four corners of ”image2” onto ”image1” using project(...) and ”homInv”. Allocate the image.
### (b)
Copy ”image1” onto the ”stitchedImage” at the right location.
### (c)
For each pixel in ”stitchedImage”, project the point onto ”image2”. If it lies within image2’s boundaries, add or blend the pixel’s value to ”stitchedImage” When finding the value of image2’s pixel use bilinear interpolation.
### (d)
Compute the Harris corner detector, find matches, run RANSAC and stitch the images ”Rainier1.png” and ”Rainier2.png”. Save the stitched image as ”3.png”. It should look like the image ”Stitched.png”.
## Problem 4: Panorama
Create panorama images
### (a)
Create a panorama that stitches together the six Mt. Rainier photographs, i.e. , ”Rainier1.png, ..., Rainier6.png”. The final result should look similar to ”AllStitched.png”.
### (b)
Create your own panorama using three or more images. You must capture the images yourself, and not find them on the web. I would recommend downsampling them before stitching, i.e. , make them approximately the same size as the images in the homework assignment.