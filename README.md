# NumPy Program: Column-wise Sorting of a 2D Array
# Aim
To write a NumPy program that sorts the elements in each column of a given 2D array in ascending order.

# Algorithm
Import NumPy: Start by importing the NumPy library.
Get Input: Accept a 2D NumPy array from the user.
Sort Column-wise: Use the np.sort() function with axis=0 to sort each column in ascending order.
Store Result: Store the sorted result in a new array.
Display Output: Print the original array and the column-wise sorted array.
# Program
```
import numpy as np

original_array = np.array([[12, 5, 7],
                           [4, 9, 2],
                           [8, 1, 6]])


sorted_array = np.sort(original_array, axis=0)


print("Original Array:")
print(original_array)

print("\nColumn-wise Sorted Array:")
print(sorted_array)
```

# Output
![alt text](<Screenshot 2025-10-20 152001.png>)
# Result

# NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y
# Aim
To write a Python program using NumPy that finds the indices where elements in array x are greater than or equal to their corresponding elements in array y.

# Algorithm
Import NumPy: Import the NumPy library.
Define Arrays: Define two NumPy arrays, x and y, with the same shape (i.e., same number of elements).
Use Boolean Indexing:
x > y gives a boolean array where elements of x are greater than y.
x == y gives a boolean array where elements of x are equal to y.
Find Indices: Use np.where() to get the indices where the conditions x >= y are satisfied.
Print Indices: Print the indices where the condition holds true.
# Program
```
import numpy as np


x = np.array([[10, 20, 30],
              [40, 50, 60]])

y = np.array([[5, 25, 30],
              [45, 45, 70]])


greater_than = x > y
equal_to = x == y


condition = x >= y
indices = np.where(condition)


print("Array x:")
print(x)

print("\nArray y:")
print(y)

print("\nBoolean array where x > y:")
print(greater_than)

print("\nBoolean array where x == y:")
print(equal_to)

print("\nIndices where x >= y:")
print(indices)
```

# Output
![alt text](<Screenshot 2025-10-20 151921.png>)
# Result

# NumPy Program: Replace the Second Column in a 2D Array
# Aim
To write a NumPy program that deletes the second column from a given 2D array and inserts a new column at the same position.

# Algorithm
Import NumPy: Start by importing the NumPy library.
Get Input: Get a 2D NumPy array and a new column (as another array) from the user.
Delete Column: Use np.delete() to remove the second column (index 1) from the original array.
Insert Column: Use np.insert() to insert the new column at the second column's original position.
Display Result: Print the updated array with the replaced column.
# Program
```
import numpy as np

original_array = np.array([[1, 2, 3],
                           [4, 5, 6],
                           [7, 8, 9]])

new_column = np.array([10, 11, 12])

array_without_second_column = np.delete(original_array, 1, axis=1)

updated_array = np.insert(array_without_second_column, 1, new_column, axis=1)

print("Original Array:")
print(original_array)

print("\nUpdated Array (with replaced second column):")
print(updated_array)
```

# Output
![alt text](<Screenshot 2025-10-20 151828.png>)
# Result

# Pandas Program: Create and Display a DataFrame with Custom Index Labels
# Aim
To create and display a DataFrame using the Pandas library in Python from a given dictionary, and apply specific index labels to the rows.

# Algorithm
Import Libraries: Import the required libraries – pandas and numpy.
Create Dictionary: Define a dictionary exam_data with keys: 'name', 'score', 'attempts', and 'qualify'.
Index Labels: Create a list of custom index labels called labels.
Create DataFrame: Use pd.DataFrame() to create the DataFrame by passing the dictionary and index labels.
Display Output: Display the DataFrame using print() or by simply calling the DataFrame variable.
# Program
```
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

print(df)
```

# Output
![alt text](<Screenshot 2025-10-20 151749.png>)
# Result

# Pandas Program: Join Two DataFrames Along Rows
# AIM
To write a Python program using Pandas to join two DataFrames along rows (row-wise concatenation) and assign all data to a new DataFrame.

# ALGORITHM
Import Libraries: Import the pandas library.
Create First DataFrame: Use a dictionary to create student_data1.
Create Second DataFrame: Use another dictionary to create student_data2.
Concatenate DataFrames: Use pd.concat() with axis=0 to concatenate both DataFrames row-wise.
Display Result: Print the new combined DataFrame.
# Program
```
import pandas as pd

student_data1 = {
    'name': ['Alice', 'Bob'],
    'score': [85, 90],
    'grade': ['A', 'B']
}

student_data2 = {
    'name': ['Charlie', 'David'],
    'score': [88, 92],
    'grade': ['B+', 'A+']
}

df1 = pd.DataFrame(student_data1)
df2 = pd.DataFrame(student_data2)

combined_df = pd.concat([df1, df2], axis=0)

print(combined_df)
```

# Output
![alt text](<Screenshot 2025-10-20 151547.png>)
# Result