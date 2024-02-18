# Below is a messy dataset representing student information

import pandas as pd

# Messy dataset
data = {
    'Student_ID': [1, 2, 3, 4, 5],
    'First_Name': ['Hindatu', 'Salma', 'Khadija', 'Hafsat', 'Sakina'],
    'Last_Name': ['Ibrahim', 'Isah', 'Hussaini', 'Kabiru', 'Salisu'],
    'Age': [20, '22', 24, '21', ''],
    'Grade': ['A', 'B', 'C', 'D', '']
}

df = pd.DataFrame(data)

# Inspect the Data
print("Original Dataset:")
print(df.head())
print(df.info())

# Handle Missing Values
df.replace('', pd.NA, inplace=True)
df['Age'] = pd.to_numeric(df['Age'], errors='coerce')
df['Grade'].fillna('Unknown', inplace=True)

# Correct Data Types
df['Age'] = df['Age'].astype('Int64')

# Standardize Data
df['Grade'] = df['Grade'].str.upper()

# Handle Duplicates
df.drop_duplicates(inplace=True)

# Index Adjustment
df.reset_index(drop=True, inplace=True)

# Verify the Cleaned Data
print("\nCleaned Dataset:")
print(df.head())
print(df.info())


# The script above used Pandas to clean and preprocess a messy dataset, documenting the steps taken during the cleaning process
