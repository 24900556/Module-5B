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
