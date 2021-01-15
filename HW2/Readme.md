# Problem One
Using homography matrix project image1 to the forward view and image2 on the LCD video wall inside the image3. (Firstly, you need to find 4 match points between source and destination images to compute the homography matrix)

# Problem Two
### Part a
Find the essential matrix that transforms the views 1-2, 2-3, 1-3 (without employing packages).

### Part b
Investigate that transforming 1 to 3 is equivalent to inverse transformation of which two transformations (calculate and print corresponding translation/rotation matrices in your code).

### Part c
Find the essential matrices between each two views using python packages.

### Part d
Repeat (Part b) for new essential matrices.

### Part e
Find the MSE of the essential matrices obtained by using 8-point algorithm and python packages for each transformations 1-2, 2-3, 1-3.