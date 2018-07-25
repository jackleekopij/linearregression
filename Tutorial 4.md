# Python Course week 4. 
This week is all about reading and writing files, with a direct focus on *.csv*s

## Contents:
  - [Types of files](#types-of-files)
  - [Reading a csv](#reading-a-csv)
  - [Writing a csv](#writing-a-csv)
  - [Excel working with spreadsheets](#excel-working-with-spreadsheets)

  
## Types of files
A common file that is very useful to n important component of computer science deals with a concept termed I/O (input/output). I/O is concerned with how computers 
store, read and save data. Specifically there are many different ways to store data, with popular methods are *.csv*, *.xlsx* and *.txt* files. Today, we will look at *.csv* and briefly *.xlsx* files. *.csv* files can be thought of as a store of tabular data, think an excel spreadsheet.


### Writing a csv
*.csv* stands for *comma seperated values* which is method used to store data. These types of files provide a logical way to 
store data in a tabular format. The following can be seen as a .csv
```csv
Index, height, age
1, 176, 24
2, 178, 67
3, 165, 45
4, 192, 42
5, 230, 32
```

In Python, it is simple to write you own *.csv*. First, open Python and type the following:
```python
import csv

my_list = [1, 3, 5]

with open('my_first_csv.csv', 'w') as csv_file:
  wr = csv.writer(csv_file)
  wr.writerow(my_list)
```
**Task 1.1**
Use Python to create a *.csv* that writes a list to .csv
```python 
my_second_list = [2, 4, 6, 8]

with open('my_second_csv.csv', 'w') as csv_file: 
  wr = csv.writer(csv_file)
  wr.writerow( ? )
```

**Task 1.2**
Use Python to create a *.csv* that stores the lists 'my_third_list' and 'my_fourth_list'. 
```python
import csv

my_third_list = [1, 3, 5, 7]
my_fourth_list = [2, 4, 6, 8] 


with open('my_third_csv.csv', 'w') as csv_file3:
  wr = csv.writer(csv_file3)
  wr.writerow( ? )
  wr.writerow( ? )
``` 

**Task 1.3** 
Use Python to first create a list of lists and then use a *for loop* to iterate over the list of lists to writing each list to a new row of a *.csv*. Hint: Google 'how to create a list of lists'.
```python
import csv

my_fifth_list = [1, 3, 5, 7]
my_sixth_list = [2, 4, 6, 8] 
my_seventh_list = [9, 10, 11, 12] 
my_list_of_lists = [?, ?, ?]


with open('my_third_csv.csv', '?') as csv_file3:
  wr = csv.writer(csv_file3)
  
for i in ?:
  wr.writerow( ? )

``` 


### Reading a csv 
From the **linearregression** directory, download the my_first_csv.csv. In the below code you will learn how to load a *.csv* file.
```python
with open('my_first_read_csv', 'r') as csv_file_read: 
  read = csv.reader(csv_file_read)
  data = [ ] 
  for element in read:
    data.append(element)
 ```
 **Task 2.1**
 From the **linearregression** directory, download the my_first_csv.csv. The data looks like 
 ```csv
 15, 35, 55
 1, 2, 42
 ```
 Your job is to read in the *.csv* and print out the value 42 by referencing the list you created named 'data'
 
 ```python
with open('my_second_read_csv', 'r') as csv_file_read: 
  read = csv.reader( ? )
  data = [ ] 
  for ? in ?:
    data.append( ? )
    
 print( ? )
 ```
 
 
  **Task 2.2**
 From the **linearregression** directory, download the my\_first\_csv.csv. The data looks like 
 ```csv
 15, , 55
 1, 2, 42
 "a string", "another string", "a final list"
 ```
 Your job is to read in the *.csv* as a lists of lists, turn the list of lists into a list (more information on this can be found [here](https://stackoverflow.com/questions/952914/making-a-flat-list-out-of-list-of-lists-in-python), store all the strings from the *.csv* in the list *flat_list* and print this list. 
 
 ```python
with open('my_second_read_csv', 'r') as csv_file_read: 
  read = csv.reader( ? )
  data = [ ] 
  for ? in ?:
    data.append( ? )
    
 flat_list = [ ]
 for ? in data:
    for element in list:
      if isinstance( ? , string)
        flat_list.append( ? )
  
 print( ? )
 ```

## Excel working with spreadsheets
Excel is an integral part of many businesses due to the ability to easily store, manipulate and save large amounts of relational data.
To work with *.xlsx* files you first need to install (download from the PyPi repository) the module *openpyxl*. To do this:
1. Click the 'start panel'. 
2. Type in 'command prompt' and press 'enter'. 
3. In the black box that appears, type ```python pip install openpyxl ```
Note: if the above fails, ensure you are one the Wi-Fi network 'wsa'. 

### Reading a .xlsx
With *openpyxl*, reading from excel spreadsheets is easy. However, one common error is the '[Error 13] Permission denied error' 
which is a result of trying to open an excel spreadsheet that is currently open. If you encounter this error, ensure the spreadsheet
you are referencing is closed.

Download the excel file in the **linearregression** directory. 
### Open a spreadsheet
The below code will get 
```python
from openpyxl import Workbook
from openpyxl import load_workbook
wb2 = load_workbook('my_first_xlsx.xlsx')

ws = wb2.active
```

### Manipulate the work book
You can reference the cell **A1** with the following:
```python
ws['A1']
```
or all the cells in rows 2 to 5 with 
```python
ws[2:5]
```

Use [this reference](https://openpyxl.readthedocs.io/en/default/tutorial.html) to set the value of cell D10 to "my\_first\_cell".

### Save the workbook
Use the following function to update your excel sheet
```python
wb2.save('Updated_workbook.xlsx')
```

Open this file and view the output.
