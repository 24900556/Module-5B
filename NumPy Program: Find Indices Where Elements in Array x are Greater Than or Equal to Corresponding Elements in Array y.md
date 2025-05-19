# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program

         import numpy as np
         x = np.array([5, 8, 3, 10, 6])
         y = np.array([3, 8, 7, 2, 6])
         
         condition = x >= y
         
         indices = np.where(condition)[0]  # [0] to get indices from the tuple
         
         print("Array x:", x)
         print("Array y:", y)
         print("Indices where x >= y:", indices)


## Output

![Screenshot 2025-05-20 050817](https://github.com/user-attachments/assets/f6ef7897-5cd7-4d72-b42b-a0169835391f)

## Result
 Thus, the program is verified successfully.
