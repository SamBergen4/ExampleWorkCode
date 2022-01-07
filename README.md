This outlines the assignment I was given!
 
-------------
## Part1: Array Manipulations   

You are going to demonstrate the following on an array of int, sized with __10 elements__. You can fill the array with whatever values you would like, but can only initialized once. Each process must be **programmatically** executed (probably using for loops). We will be changing the values as we grade. You may even want the user to input values where appropriate. You are going to need to manipulate the arrays, not just pull the numbers out.

* __Reverse the array__. Example: Given the array 1 6 3 9 12 5, manipulate into an array 5 12 9 3 6 1
* __Double every odd element__. Example: Given the array 1 2 3 4 5 6. Double every odd element, to make the array all even: 2 2 6 4 10 6
* __Insert into an array__. Example: Given the array 8 6 4 2, insert 1 into the 3rd element. Resulting in: 8 6 1 4. Move everything to the right, and drop (overwrite) the last element. Either show that you can replace every element, or replace a user input element, or random elements.
* __Remove element from array.__ Example: Given the array 2 3 4 6 8 10, remove the 2nd element. Resulting in 2 4 6 8 10 0. Move everything to the left, add a zero to the end. Same as above, complete removal, or random removal or user input based removal.  
  


-------
## Part 2: Phone Number Translator   

You are going to write a program that parses a text based phone number into the actual phone number that it represents. As an example, 1-800-WHITWORTH represents 18009448967 (notice that phone numbers are only 11 digits!).  


The user will input a string, the program will output the number that needs to be dialed. This output needs to be just numbers, and only 11 of them! Nothing else (you can have other text on the screen for proper formatting and documentation, but the ‘answer’ will only be numbers).  





|          |         |         |
|----------|---------|---------|
| 1        | 2 (abc) | 3 (def) |
| 4 (ghi)  | 5 (jkl) | 6 (mno) |
| 7 (pqrs) | 8 (tuv) | 9 (wxyz)|
| *        | 0       | #       |


-------------
## Employee Hour Statistic Tool   

You are going to write a program to help a manager find statistics on the hours worked by their employees. This company has 10 employees, and is open 7 days a week.  

You are going to implement a two dimensional array to hold hourly work data for the employees. We would suggest making this array: `[employeeIndex][DayIndex]`. You need to __write a function to fill the array.__ Make sure you do this logically. Hints on 'logically': an employee can't work more than 24 hours (probably no more than 12 hours, you might even say 8 hours), each employee should probably have some days off, and you should probably have at least one person working per day. This function should probably use `rand()`.


After setting up this array you are going to write a number of functions to form a report:  

* Display function to output the table of hours in a reasonable format.
* Total hours function to report the number of hours worked per week for each employee (or a single employee, and call the function a number of times).
* Daily Hours function to report the total hours worked for each day.
* Warning function to report if any of the shifts are longer than 8 hours, if any employee is working less than 20 hours a week and if any employee is working more than 40 hours.

