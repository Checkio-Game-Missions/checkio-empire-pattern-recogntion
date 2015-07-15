In our computer, a slice image and pattern can be represented as a binary matrix, 
where the main atoms (X and Z) are represented with 1 and 0. 
You should write a program to search a binary matrix (pattern) within another binary matrix (image). 
The recognition process consists of scanning the image matrix row by row (horizontal scanning) 
and marking patterns when one is located in the image. 
To mark a located pattern, the program must change 1 to 3 and 0 to 2. 
The result will be the image matrix with the located patterns marked.

The patterns in the image matrix will never cross because the value of each number in the pattern is immediately changed when marked.

```
Pattern     Image

  1 0       0 1 0 1 0
  1 1       0 1 1 0 0
            1 0 1 1 0
            1 1 0 1 1
            0 1 1 0 0

   1st         2nd         3rd
0 3 2 1 0   0 3 2 1 0   0 3 2 1 0
0 3 3 0 0   0 3 3 0 0   0 3 3 0 0
1 0 1 1 0   3 2 1 1 0   3 2 1 3 2
1 1 0 1 1   3 3 0 1 1   3 3 0 3 3
0 1 1 0 0   0 1 1 0 0   0 1 1 0 0
```
