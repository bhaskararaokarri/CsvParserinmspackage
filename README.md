# Custom made csvpaserinms Package

### documentation 
```
 The main theme of this project is to read the data from csv file Perform crud operations in a csv file and
Writes modified data into csv file.
```

### Methods in the module
```
		writeCsv ---> Writes the data in a csv file format in a file
		rowInsertCsv --> Inserts a row in a specific index with the given data
		rowAppendCsv ---> Appends a row to the existing file at the end of the file with given data
		rowDeleteCsv --->Deletes a specific row in the given file
		rowReplaceCsv ---> Replaces a row to the existing file at a given index with given data
		modifiedSpecificColumnInRowCsv ---> Modifies the specific data with given data in a csv file
		InsertColumnCsv --->Inserts specific Column in an existing file with given data
		deleteSpecificColumnCsv ---> Deletes a column with given index number in a csv file
		deleteDataFromCsvFile ---> Deletes the whole data from the csv file where file path is given
		removeCsvFile ---> Deletes the csv file if the file path is given
		readCsv ---> Read all data the csv file if the file path is given
		readLineCsv ---> Read singleLine
		UpdateExistingCsvFile --> Updates the given file with the new data

```

## Application or usage

```
the main csvparser package is application is perfom curd operations on a user provide file 
```

## Instructions for packaging
```
python3 -m pip install --user --upgrade setuptools wheel
```

Now run this command from the same directory where setup.py is located:
```
python3 setup.py sdist bdist_wheel
```

This command should output a lot of text and once completed should generate two files in the dist directory:
`One whl file` and `One gz file`


## create virtual environment
```
dist/
  csvparseinmsoperations_bhaskara_rao-1.0.0-py3-none-any.whl
  csvparseinmsoperations-bhaskara-rao-1.0.0.tar.gz
  
```
 create virtualenvironment in your local pc 
```
instalition for virtual env : pip instal virtualenv
```
create directory :
command :
```
	virtualenv dirctoryName
```

 now you are activate the virtualenvironment
command :
```
	directoryname\scripts\activate.bat
```
after goto your ProjectLocation there you opened python in a terminal

import class from your package
command:
```
	from csvparser.main import CsvParser
```
create a object to that class
command:
```
	parser = CsvParser
```
byusing that objects you can call all methods inside csvparserpackage
command:
```
	parser.readCsv("filepath")
	parser.writeCsv("filepath",data)
	parser.readLineCsv("filepath")
	parser.rowAppendCsv(data,index)
	parser.removeCsvFile("fiepath")
	parser.updateExistingCsvFile()
	parser.rowInsertCsv(listvalue,rowindex)
	parser.rowDeleteCsv(rowindex)
	parser.rowReplaceCsv(value,index)
	parser.modifySpecificColumnInRowCsv(row_no_index,index,value)
	parser.insertColumnCsv(values,index)
	parser.deleteSpecificColumnCsv(index)
	parser.deleteDataFromCsvFile(filepath)
	parser.removeCsvFile(filepath)
	parser.raedCsv(filepath)
	parser.readLineCsv(filepath,lineNo)
```