**Precondition:**
```python
0 < len(image) <= 10
all(len(image[0]) == len(row) and 0 < len(row) <= 10 for row in image)
0 < len(pattern) <= 10
all(len(image[0]) == len(row) and 0 < len(row) <= len(image[0]) for row in pattern)
len(pattern) < len(image)
```