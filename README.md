# LM9: Arrays
CS1 - Whitworth University  
Dr. Qian Mao and Scott Griffith  
Due: 11/15/21 
Source: Whitworth CS Faculty  

## Overview
You should be applying all the good things we have been working on: functionalization, good commenting, proper variable re-use. Just because we are doing something different does not mean you should forget all that previous good stuff.

## Grade Break Down
| Part   |                           |    Points    |
|--------|---------------------------|--------------|
| Part 1 | Array Manipulations       |         0/20 |
| Part 2 | Phone Number Translator   |         0/30 |
| Part 3 | Employee Hour Tool        |         0/50 |
|        |                           | Total: 0/100 |

It does not appear that you attempted this Learning Module? If you need help or are having trouble starting, there is tutoring in Johnston 304 7:30-9:00pm Monday/Tuesday and 7:00-8:00pm Thursday/Sunday.

### Code Requirements
- Follow style guide
- Good and proper comments
- Appropriate variable re-use
- Read the problem requirement closely 
- Functions should not use `cout` unless then *need* to
 
-------------
## Part1: Array Manipulations (20 pts)  

The goal of this is to get some practice using arrays. If you are using other tools / methods, you should reconsider what you are doing. 

You are welcome to keep everything in one function. You can still define and implement functions (We would suggest it) but We will not be grading you on your use of functions for this part. If it makes more sense for you to pass arrays in an out of functions you can:

`void reverseArray(int array[], int size)` - Arrays are always passed by reference, so this will change the array in the original context as well. For single dimensional arrays (what we are doing) you don't need to define the size, you can just refer to it as an array with the `[]`.  

You are going to demonstrate the following on an array of int, sized with __10 elements__. You can fill the array with whatever values you would like, but can only initialized once. Each process must be **programmatically** executed (probably using for loops). We will be changing the values as we grade. You many even want the user to input values where appropriate. You are going to need to manipulate the arrays, not just pull the numbers out.

* __Reverse the array__. Example: Given the array 1 6 3 9 12 5, manipulate into an array 5 12 9 3 6 1
* __Double every odd element__. Example: Given the array 1 2 3 4 5 6. Double every odd element, to make the array all even: 2 2 6 4 10 6
* __Insert into an array__. Example: Given the array 8 6 4 2, insert 1 into the 3rd element. Resulting in: 8 6 1 4. Move everything to the right, and drop (overwrite) the last element. Either show that you can replace every element, or replace a user input element, or random elements.
* __Remove element from array.__ Example: Given the array 2 3 4 6 8 10, remove the 2nd element. Resulting in 2 4 6 8 10 0. Move everything to the left, add a zero to the end. Same as above, complete removal, or random removal or user input based removal.  
  
Make sure you are fully demonstrating your code to the user and that it is formatted well. This means we should be able to run your code and see that it works!

-------
## Part 2: Phone Number Translator (30 pts)  

You are going to write a program that parses a text based phone number into the actual phone number that it represents. As an example, 1-800-WHITWORTH represents 18009448967 (notice that phone numbers are only 11 digits!).  

For this program you must develop and use at least the following function prototypes:  

```cpp
char charToNum(char ch);
void stringToPhoneNumber(string input_st, string& output_st);  
```

The user will input a string, the program will output the number that needs to be dialed. This output needs to be just numbers, and only 11 of them! Nothing else (you can have other text on the screen for proper formatting and documentation, but the ‘answer’ will only be numbers).  

Strings act very similar to arrays. You can access individual elements using the accessor function `[]` (We would suggest playing around with the following code):  

    string test = "LMs are Fun!";
    for(int i = 0; i < test.length(); i++){
        cout << test[i] << " ";
    }


If you were wondering, We were partially inspired by this: https://imgur.com/a/4f3XB

Normal phone layout:  
https://en.wikipedia.org/wiki/Telephone_keypad#/media/File:Telephone-keypad2.svg 

|          |         |         |
|----------|---------|---------|
| 1        | 2 (abc) | 3 (def) |
| 4 (ghi)  | 5 (jkl) | 6 (mno) |
| 7 (pqrs) | 8 (tuv) | 9 (wxyz)|
| *        | 0       | #       |


-------------
## Employee Hour Statistic Tool (50 pts)  

You are going to write a program to help a manager find statistics on the hours worked by their employees. This company has 10 employees, and is open 7 days a week.  

You are going to implement a two dimensional array to hold hourly work data for the employees. We would suggest making this array: `[employeeIndex][DayIndex]`. You need to __write a function to fill the array.__ Make sure you do this logically. Hints on 'logically': an employee can't work more than 24 hours (probably no more than 12 hours, you might even say 8 hours), each employee should probably have some days off, and you should probably have at least one person working per day. This function should probably use `rand()`.

For passing in 2D arrays into functions, see 8.4 in the book (pg. 314)

After setting up this array you are going to write a number of functions to form a report:  

* Display function to output the table of hours in a reasonable format.
* Total hours function to report the number of hours worked per week for each employee (or a single employee, and call the function a number of times).
* Daily Hours function to report the total hours worked for each day.
* Warning function to report if any of the shifts are longer than 8 hours, if any employee is working less than 20 hours a week and if any employee is working more than 40 hours.

__Function design warning:__ Be careful about how you define your functions. Be intentional about what information is being passed in, what information is being returned, what information is being printed to the screen and what needs to be passed by reference. Remember the only function that should be cout-ing anything is your display and warning function!

__Extra credit heads up:__ There is a lot you can do with this to get extra credit. Remember to think broadly about the problem and what information might be helpful to a user.
