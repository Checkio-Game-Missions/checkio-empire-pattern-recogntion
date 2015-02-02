With it a slice image and a pattern can be represented as a binary matrix, 
where our main atoms (X and Z) are represented with 1 and 0.
You should write a program to search a binary matrix (a pattern) within another binary matrix (an image).
The recognition process consists of scanning the image matrix row by row (horizontal scanning) and
when a pattern is located on the image, the program must mark this pattern. 
To mark a located pattern change 1 to 3 and 0 to 2.
The result will be the image matrix with the located patterns marked.

The patterns in the image matrix are not crossed, because you should immediately mark the pattern.

![pattern](pattern.svg)
