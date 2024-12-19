# Day 4 Exercise – Conversion Calculator

## Goal

In today's exercise, you will write Python code that converts a given value from its original unit to a different unit.

You will use the data file, `conversionMeasures.csv`, where each line of the data file is three pieces of data separated by commas: `from_unit,conversion_factor,to_unit`.

```
kilometer,1000,meter
meter,100,centimeter
inch,2.54,centimeter
...
```

Your code will use this information to convert a value from one unit to another.

The conversion equation for all of these lines is `from_unit_value` x `conversion_factor` = `to_unit_value`.

Your code should be able to convert the following test cases:

```
from_unit = "pint"
test_value = 2.5
to_unit = "mL"

from_unit = "cubic foot"
test_value = 30
to_unit = "liter"

from_unit = "slug"
test_value = "4.8"	# Yes, you should write your code to handle values that are entered as strings
to_unit = "pound"

from_unit = "slug"
test_value = 27.0
to_unit = "snail" # See 'Errors to anticipate' below
```

By the end of day, your code should:

* Read and store the conversion data from the csv file in some object (list of lists, dictionary of dictionaries, etc.)
* Provide a way to find the correct conversion factor from your data object
* Include a function to convert between units
* Print out a full sentence response with the final answer
* Anticipate some errors (more on this below)
* Run your code on the provided test examples

## Getting Started in Colab

To get started, you will first need to make a [**new notebook in Colab** that runs Python 3](https://colab.research.google.com/github/nuitrcs/pythonBootcamp_4Day/blob/main/day4morning.ipynb). You can save a working copy of this notebook by clicking on `File > Save a copy in Drive`. This way you can come back to your work even after closing the notebook.

To use the csv file, you will need to run a cell at the top of your notebook that says:

```
!wget https://raw.githubusercontent.com/nuitrcs/pythonBootcamp_4Day/main/conversionMeasures.csv
```

## Parts Overview

Today's exercise will be split into 3 main parts. For each part, we will spend 30 minutes together to understand what should be accomplished, and then you will spend 45 minutes to 1 hour writing the code.

### Part 1

Read `conversionMeasures.csv` and store the information as a python data object. There are multiple options for data types (list of lists, dictionary of lists, dictionary of dictionaries, etc.) depending on how you aim to find the conversion in part 2.

### Part 2

Given `from_unit` and `to_unit`, identify the correct conversion factor using the data object created in part 1. After identifying the conversion factor, convert unit using the formula.

### Part 3

Finalize the code by making it print out a full sentence response with the final answer. In this part, you will also explore possible errors and consolidate your code to deal with this errors.

## Errors to anticipate

While working on **part 3**, or even before that, you might encounter problems that produce error in your code.

1.	Someone might give the initial value as a string instead of a float/integer.
2.	Someone might request a final unit that is not in your data – your code should print out an error message. Here’s a sample to test for this error:

```
test_unit = "slug"
test_value = 27.0
final_unit = "snail"
```

## Tips

* You might write out the steps you need to complete each task before you start coding
* Take it one step at a time
* We highly recommend trying to figure out what steps need to taken to finish each part. However,if you find yourself stuck with a problem, you can reference [`day4morning_help_detail.md`](https://github.com/nuitrcs/pythonBootcamp_4Day/blob/main/day4morning_help_detailed.md), which contains more detailed steps

## Python notebook and script organization

Code should be organized in the following order:

1. A description of what the notebook or script does, what type of data you must or can use (file type, required columns, etc.), and what products (files, visualizations, reports, etc.) are made.
2. Import any packages used
3. Define any input or output filenames, saving the file paths as variables
4. Any data structures that will be used in the code (dictionaries, lists, etc.)
5. Define any custom functions or objects that will be used in the body of the code
6. Body of the code (calling functions, looping, cleaning data, doing calculations, etc.)

## BONUS CHALLENGES

1.	Someone might give a test or final unit that has different capitalization than how it is presented in the csv file. Edit your code so that it can still process this sample:

```
test_unit = "KM/H"
test_value = 8.4
final_unit = m/Sec
```

2.	In the csv file, not all the units are included on both sides of the conversion factor. Someone might give you a test unit from the right side of the factor and ask you to convert it to the unit on the left side, which would require division instead of multiplication. Edit your code so that it can process this sample:

```
test_unit = "ergs"
test_value = 8.4
final_unit = "joule"
```

3.	Advanced Challenge: there’s a function called `input()` that can collect data from the user of your code in real time. Here’s a link to a website that works through the `input()` function (top half of the page only – stop before the Tkinter section): https://datatofish.com/input-function-python/. Try to use the `input()` function to collect the `from_unit`, `test_value`, and `to_unit` values.
