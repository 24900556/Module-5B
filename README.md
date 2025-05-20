# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
      import numpy as np
      
      array = np.array([[12, 5, 7],
                        [4, 8, 2],
                        [9, 3, 6]])
      
      sorted_array = np.sort(array, axis=0)
      
      print("Original Array:")
      print(array)
      
      print("\nColumn-wise Sorted Array (Ascending):")
      print(sorted_array)

## Output
![Screenshot 2025-05-20 045707](https://github.com/user-attachments/assets/b99b0753-f6f0-4592-aef6-4cc1ee2801b8)

## Result
 Thus, the program is verified successfully.

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

 # NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program

    import numpy as np
    
    original_array = np.array([
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]
    ])
    
    new_column = np.array([20, 50, 80])  # Must have same number of rows
    array_without_second_col = np.delete(original_array, 1, axis=1)
    updated_array = np.insert(array_without_second_col, 1, new_column, axis=1)
    print("Original Array:")
    print(original_array)
    
    print("\nNew Column:")
    print(new_column)
    
    print("\nUpdated Array:")
    print(updated_array)

## Output
![Screenshot 2025-05-20 051132](https://github.com/user-attachments/assets/3ca02018-d545-40ea-af4e-772e95650e0e)

## Result
 Thus, the program is verified successfully.

 # Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program
    import pandas as pd
    import numpy as np
    exam_data = {
        'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily'],
        'score': [12.5, 9.0, 16.5, np.nan, 9.0],
        'attempts': [1, 3, 2, 3, 2],
        'qualify': ['yes', 'no', 'yes', 'no', 'no']
    }
    labels = ['a', 'b', 'c', 'd', 'e']
    df = pd.DataFrame(exam_data, index=labels)
    print("DataFrame with custom index labels:")
    print(df)

## Output
![Screenshot 2025-05-20 051537](https://github.com/user-attachments/assets/df83e999-1902-4801-a379-19050e95872f)

## Result
 Thus, the program is verified successfully.

 # 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program
    import pandas as pd
    student_data1 = {
        'name': ['Alice', 'Bob'],
        'score': [85, 90],
        'attempts': [1, 2],
        'qualify': ['yes', 'no']
    }
    df1 = pd.DataFrame(student_data1)
    student_data2 = {
        'name': ['Charlie', 'David'],
        'score': [95, 88],
        'attempts': [3, 1],
        'qualify': ['yes', 'yes']
    }
    df2 = pd.DataFrame(student_data2)
    combined_df = pd.concat([df1, df2], axis=0, ignore_index=True)
    print("Combined DataFrame (Row-wise):")
    print(combined_df)

## Output
![Screenshot 2025-05-20 051711](https://github.com/user-attachments/assets/60424a69-e8af-4e73-a15e-a03ca0585a06)

## Result
 Thus, the program is verified successfully.
