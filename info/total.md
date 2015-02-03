Let's continue improve our recognising systems.
We will examine slice images of crystals, find some pattens and mark them.
With it a slice image and a pattern can be represented as a binary matrix, 
where our main atoms (X and Z) are represented with 1 and 0.
You should write a program to search a binary matrix (a pattern) within another binary matrix (an image).
The recognition process consists of scanning the image matrix row by row (horizontal scanning) and
when a pattern is located on the image, the program must mark this pattern. 
To mark a located pattern change 1 to 3 and 0 to 2.
The result will be the image matrix with the located patterns marked.

The patterns in the image matrix are not crossed, because you should immediately mark the pattern.

![pattern](pattern.svg)

**Input:** Two arguments. A pattern as a list of lists and an image as a list of lists. 

**Output:** The marked image as a matrix as a list of list.
**Example:**

```python
mark_patterns([[1, 0], [1, 1]],
              [[0, 1, 0, 1, 0],
               [0, 1, 1, 0, 0],
               [1, 0, 1, 1, 0],
               [1, 1, 0, 1, 1],
               [0, 1, 1, 0, 0]]) == [[0, 3, 2, 1, 0],
                                     [0, 3, 3, 0, 0],
                                     [3, 2, 1, 3, 2],
                                     [3, 3, 0, 3, 3],
                                     [0, 1, 1, 0, 0]]
mark_patterns([[1, 1], [1, 1]],
              [[1, 1, 1],
               [1, 1, 1],
               [1, 1, 1]]) == [[3, 3, 1],
                               [3, 3, 1],
                               [1, 1, 1]]
```
**How it is used:**

As we can see in the first paragraph, this task is simple monochromatic pattern recognition.
You can take a monochrome image and find various subimages inside such as the alien spaceships in the Galaxy Game ;-)
**Precondition:**
```python
0 < len(image) <= 10
all(len(image[0]) == len(row) and 0 < len(row) <= 10 for row in image)
0 < len(pattern) <= 10
all(len(image[0]) == len(row) and 0 < len(row) <= len(image[0]) for row in pattern)
len(pattern) < len(image)
```