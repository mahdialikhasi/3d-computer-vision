Two images are given in files ‘img1.png’ and ‘img2.png’. The file ‘points_inlier.mat’ includes 20 pair of corresponding points in the images.

### Part a
Compute the fundamental matrix using these points. Show points and epipolar lines on images

### Part b
Now using 'points.mat' we know half of the pairs are inliers and the other
half are outliers. Using RANSAC and the 8-point algorithm, how many iterations are needed to ensure getting a correct fundamental matrix with 99% probability? Implement a program to find the fundamental matrix using
these points.

### Part c
The real fundamental matrix between the images is given in 'info.mat'. Compare the results of parts a and b, with this matrix and illustrate the epipolar geometry yielded by each matrix