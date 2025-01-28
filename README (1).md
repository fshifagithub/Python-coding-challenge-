
# Python coding challenge 

This Python script is designed to extract groups mentioned in a specified column of a CSV file and count their occurrences. It is customizable, allowing you to input different file paths, column names, and target strings at runtime.






## Features


- Reads data from a CSV file.
- Extracts group names based on a specific pattern (`Groups : [code]<I>XXXX </I>[/code]`).
- Counts the occurrences of each group.
- Outputs the result to a text file.
- Allows customization of:
  - Input file path
  - Column name to search
  - Target string for group identification




## Installation

1. Ensure you have Python 3.7 or later installed.
2. Install the required libraries using pip:
   pip install pandas
- Python 3.7 or higher
- Libraries: `pandas`, `re`, `collections`


## Working

The provided Python script is designed to extract and count group names from a specified column in a CSV file based on a specific pattern. It begins by reading the input CSV file using the pandas library and checks if the specified column (column_name) exists in the file. The script then defines a regular expression pattern (group_pattern) to search for lines containing the target string ( "Groups") in the format Groups : [code]<I>XXXX</I>[/code]. It iterates through each row of the specified column, identifying matches to the pattern. For each match, it extracts the group names. Using Python's collections.Counter, it calculates the occurrences of each group. Finally, the results are stored in a pandas DataFrame, sorted in descending order by occurrence, and written to a text file (group_counts.txt).

## Customization
input_file = "coding challenge.csv"

column_name = "Additional comments"

target_string = "Groups"

output_file = "group_counts.txt"

## Error Handling



1.The script validates:
If the input file exists.
If the specified column is present in the CSV file.

2.Any errors will be displayed in the console.

## output

Group_name                                 Number of occurrences

Huntingdon and Liz area  -                     2
                  
SML Group GMs            -                     1 
                    
Eastend GMs              -                     3


