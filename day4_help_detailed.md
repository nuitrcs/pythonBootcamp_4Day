# Day 4 Exercise – Conversion Calculator (Detailed)


## Part 1

Store the conversion data from the csv file in some object (list of lists, dictionary of dictionaries, etc.)

1. open the file in read mode
2. save as a list of lines with f.readlines()
3. exit the with/as statement
4. create an empty list
5. loop through the lines from the file
6. for each line, remove the trailing new line character and split the line on the commas, which will make a list
7. append the list to the empty list you made above – you should have a list of lists

## Part 2

Find the correct conversion factor from your data object and make conversion.

1. Create a function to find conversion unit
   1. loop though the list of lists
   2. if the `from_unit` is equal to the item in the first position of the list and the `to_unit` is equal to the third item in the list, return the second item in the list
2. Create a function to convert between units
	1. the function should take the `test_value` and `conversion_factor` as arguments and return the new value
	2. call and test the function with your `test_value` and `conversion factor`
3. Finally, combines step 1 and step 2
   1. Use function from step 1 to find conversion unit and save that to a variable
   2. Use the output to apply conversion with function from step 2
   3. You can create a function that takes `from_unit`, `to_unit`, and `test_value` as arguments for this step

## Part 3

1. Print out a full sentence response with the final answer
2. Look for potential errors and handle them
   1. Someone might give the initial value as a string instead of float/integer
      * Attempt to convert the initial value to float
      * Handle the error by printing out what's wrong with the input and end function
   2. Someone might request a final unit that is not in your data
      * If after looping through the list of lists, there's no matching unit, print out the issue and end function
3. Run your code on the provided test examples

