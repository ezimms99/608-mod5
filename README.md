# 608-mod5

Chapter 7 Notes: 

NumPy: 
- First appeared in 2006 and is the preferred python array implementation. 
- Offers, ndarray which from this point forward we'll refer to by its synonym array. 

Creating arrays from exisiting data: 
- Import numpy module as np. 
- array function recieves as an argument an array or other collection of elements and returns a new array containing the arguments elements. 
- You can also create multidimensional arguments by using multiple [] [] 

Array Attributes: 
- An array provides attributes that enable you to discover information about its structure and contents. 
- You can check the element type with an array's dtype attribute. 
- The attribute ndim contains an array's number of dimensions and the attribute shape contains a tuple specifying an array's dimensions. 
- You can view an array's total elements using size and number of bytes required to store each element with itemsize. 
- You can iterate through a multidimensional array as if it were one-dimensional by using its flat attribute. 
- By default NumPy does not display trailing zeros in the fractional part of a floating point value. 

Filling array with specific values: 
- NumPy provides functions zeros, ones, and full for creating arrays containing 0s 1s, or a specified value. 
- np.zeros(5) populates an array with 5 zeros, np.ones((2,4), dtype=int) creates a 2x4 array with ones, full is the same just specify value. 

Creating arrays from Ranges
- NumPy's arrange function creates integer ranges. 
- np.arrange(5) will spit out array([0,1,2,3,4]) 
- The linspace function produces evenly spaces floating point ranges. 
- You can also reshape an array using reshape to transform a one-dimensional array into a multidimensional array. 
- When displaying over 1000 items or more NumPy will "hide" values. 

List versus array performance: Introducing %timeit 
- %timeit magic command times the average duration of operations. 
- After using the function it will display the average execution time. 
- Arrays typically run faster than lists. 
- -n and -r all you to customize the loop and number of loops. 
- Other iPython magics 
  - %load to read coad into IPython from a local file or URL
  - %save to save snippets to a file. 
  - %run to execute a .py file from IPython
  - %precision to change the default floating-point precision for Ipython outputs.
  - %cd to change directories without having to exit IPython first
  - %edit to launch an external editor 
  - %history to view a list of all snippets and commands you've executed in the current IPython session. 
  
  Array Operators: 
  - You can use arithmetic operators to calculate on an array. 
  - The original array will stay the same, simply the outputs will change based on arithmetic. 
  - When multiplying by a single value (scalar) NumPy populates an array of the same size to multiple by, this is called broadcasting. 
  - You can also perform arithmetic between arrays of the same shape. 
  - You can also do comparative statements on arrays and will evaluate on an element level. 
  
  NumPy Calculation Methods:
  - You can also use various methods to perform calculations on an array like mean, median, mode, var, std. 
  - You can also perform calculations on specific array dimensions known as the array's axes. 
  - Specifying axis = 0 performs on all the row values within each column. 
  
  Universal Functions: 
  - There are universal functions that performs various elemen-wise operations. 
  - sqrt calculates square root of values. 
  - Use add to add two arrays with the same shape. 
  - Multiply is also a universal function. 
  
  Indexing and Slicing: 
  - You index multiple arrays list you would a list. With the [] formate. 
  - To select a single row, specify only one index in square brackets. 
  - To select multiple sequential rows, use the slice notation --> [0:2] to select multiple rows. 
  - To select multiple non-sequential rows, use a list of row indices. 
  - You can select subsets of the columns by providing a tuple specifying the rows and columns to select. 
  - :,0 selects column 0, the : indicates which rows within the column to select which represents all rows, if a number followed this would be the row number. 
  
  Views: Shallow Copies:
  - View objects are objects that see the data in other objects, rather than having their own copies of the data.
  - Views are also known as shallow copies. 
  - The array method view returns a new array object with a view of the original array object's data. 
  - Changing the view also changes the value of the original array. 
  - You can also use a slice [:] to create a view. 
  - Trying to access elements in a view creates an IndexError. 
  
  Deep Copies: 
  - A deep copy has independent copies of the original data. 
  - The array copy method returns a new array object with a deep copy of the orginial array object's data. 
  - When doing this, modifying the original doesn't change the copy. 
  - Other types of python objects use deepcopy function. 
  
  Reshaping and Transposing:
  - reshape returns a view of the original array with the new dimensions it does not modify the original arary. 
  - resize modifies the original arrays shape. You cab take multidimensional arrays and use flatten to make it single dimensional with a deep copy. 
  - ravel produces a view of the original array
  - You can quickly transpose an array's rows and columns -- that is "flip" the array, so the rows become the columns and columnes become rows. Use .T to do this and produce a shallow copy and does not modify original array. 
  - You can combine arrays by adding more columns or more rows -- known as horizontal and vertical stacking. 
  - Combine two arrays using hstack to combine horizontalls or vstack to combine vertically. 
  
  
  
  
  
  
