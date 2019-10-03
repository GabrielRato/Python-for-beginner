## Python read and write csv files

## Python read csv files:
```python
import csv
with open('my_file.csv', newline='') as csvfile:
	# now we define how we read this file object
	reader = csv.reader(csvfile, delimiter='', quotechar='|')
	# just print every column, row by row
	for row in reader:
		print(row)
```

## The full syntax of csv.reader() is:

```python
csv.reader(csvfile, dialect='excel', **fmtparams)
```

```
## csv.reader() Parameters
##csv.dialect - The Dialect class is a container class relied on primarily for its attributes, which are used to define the parameters for a specific reader or writer instance.
##fmtparams - fmtparams keyword arguments can be given to override individual formatting parameters in the current dialect, in our case we used delimiter and quotechar, for full details check the link bellow:
```
[full parameter list](https://docs.python.org/3/library/csv.html#csv-fmt-params)

## Python write csv files()
```python
import csv
with open('my_file.csv', newline='') as csvfile:
	# now we define how we write into this file object
	writer = csv.writer(csvfile, delimiter='',
				quotechar='|', quoting=csv.QUOTE_MINIMAL)
	for row in writer:
		writer.writerow(['New value', 'Another Value'])
```

## The full syntax of csv.reader() is:

```python
csv.reader(csvfile, dialect='excel', **fmtparams)
```

```
## csv.reader() Parameters
## works in the same was as csv.reader
```

