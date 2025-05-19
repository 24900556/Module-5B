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
