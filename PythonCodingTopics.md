MAIN: Project & Intro Information , based on this any set of random questions will be asked

MAIN:
# Given a string, find the first non-repeating character in it. For example, if the input string is # # “TimesforTimes”, then output should be ‘f’ and if input string is “TimesQuiz”, then output should be # ’T’.
def simple_nonrep_char(str):
    for i in str:
        if str.count(i) == 1:
            print ("first non rep char is ", i)
            break

print(simple_nonrep_char("TimesQuiz"))
print(simple_nonrep_char("TimesforTimes"))



MAIN: Extract & print only numbers from alphanumeric string input

str = '0 abc 1 yz 2'
sum = 0
numbers = []

for s in str.split():
    try:
        numbers.append(int(s))
    except ValueError:
        pass
    
print (numbers)

MAIN: (A variation would be to extract the sequence and then sum it up too)
# Function to calculate sum of all
# numbers present in a str1ing
# containing alphanumeric characters
import re


def find_sum(givenStr):
    # Regular Expression that matches digits in between a string
    return sum(map(int, re.findall(r"\d+", givenStr)))


# Driver code
# input alphanumeric string 
# 1+121 = 122
inputString = "1abc121"
print(find_sum(inputString))

#WAP for Balancing of parenthesis 
## Python3 code to Check for
## balanced parentheses in an expression

open_list = ["[", "{", "("]
close_list = ["]", "}", ")"]

## Function to check parentheses
def check_balanced(myStr):
    stack = []
    for i in myStr:
        if i in open_list:
            stack.append(i)
        elif i in close_list:
            pos = close_list.index(i)
            if ((len(stack) > 0) and
                    (open_list[pos] == stack[len(stack) - 1])):
                stack.pop()
            else:
                return "Unbalanced"
    if len(stack) == 0:
        return "Balanced"
    else:
        return "Unbalanced"


# code to test different scenatios
string = "{[]{()}}"
print(string, "-", check_balanced(string))

string = "[{}{})(]"
print(string, "-", check_balanced(string))

string = "((()"
print(string, "-", check_balanced(string))

SAMPLE O/P: 
{[]{()}} - Balanced
[{}{})(] - Unbalanced
((() - Unbalanced

HOw to find Factorial:
 # recursively find factorial 
def factorial(n):      
    return 1 if (n==1 or n==0) else n * factorial(n - 1);  
  
# Driver Code 
num = input (“Enter the number: ”); 
fac = int (num)
print("Factorial of", fac,"is", 
factorial(fac)) 

HOw to find whether given num is Prime or NOT:
num = 11
  
#If given number is greater than 1 
if num > 1: 
      
   # Iterate from 2 to n / 2  
   for i in range(2, num): 
         
       # If num is divisible by any number between  
       # 2 and n / 2, it is not prime  
       if (num % i) == 0: 
           print(num, "is not a prime number") 
           break
   else: 
       print(num, "is a prime number") 
  
else: 
   print(num, "is not a prime number”)

How to find Largest number in Array:
def largest(arr,n): 
  
    # Initialize maximum element 
    max = arr[0] 
  
    # Traverse array elements from second 
    # and compare every element with  
    # current max 
    for i in range(1, n): 
        if arr[i] > max: 
            max = arr[i] 
    return max
  
# Driver Code 
arr = [10, 324, 45, 90, 9808] 
n = len(arr) 
Ans = largest(arr,n) 
print ("Largest in given array is",Ans) 


[ASSIGNMENT]

Collections:
Types of Collections
Features of Lists
Modification of Lists
Insert into list
Append into list
Remove from List
Sort a list
Features of Sets
Difference between list and sets
Common elements between sets
Different elements between sets
Can a tuple be edited?
How to indirectly update a tuple
Features of Dictionary
Get a value from a dictionary
Remove a value from a dictionary(del/pop)
Strings:
Concatenate string (different ways)
 
File Operations:
File operation:
Open 
•	‘r’ – Read mode which is used when the file is only being read 
•	‘w’ – Write mode which is used to edit and write new information to the file (any existing files with the same name will be erased when this mode is activated) 
•	‘a’ – Appending mode, which is used to add new data to the end of the file; that is new information is automatically amended to the end 
•	‘r+’ – Special read and write mode, which is used to handle both actions when working with a file
API Testing
 
 
3 important constructs
 
try: & except ValueError: & raise
try Continue and finally to bypass say divideByZero exception
 
Problem Solving:
 
1.      Non-repeating character in a string 
2.      Input length of array and elements of array, find sum of array elements. 
3.      Second highest number in an array of numbers          
4.      Read Json from a file and print a name if age is greater than 70. 


Problem 1:
==========
1.	Given a string split the string in the middle (left, right).
2.	Create a new string by changing the order. (e.g. new_string = right + left)
3.	Remove characters from the new string if suffix of right == prefix of left
4.	Repeat step 3 until no matching is found.
Example:
               Given_string = “abbcabaa”
               Left = “abbc”
               Right = “abaa”
               New_string = "abaa"+"abbc"
                suffix of abaa is a, prefix of abbc is a and both are matching
                new_string = “abbbc”
               suffix of ab is b, prefix of bbc is b and both are matching
               new_string = “ac”
                suffix of a is a, prefix of c is c and both are not matching. 

Hence final output = “ac”

Problem 2:
==========
1.	Given list of strings:
2.	Form a string with given indices
3.	Find character at given position
Example:
  Number of strings = 5
  Strings:
                “aaaaa”
                “bbbbb”
                “ccccc”
                “ddddd”
                “eeeee”
Problem output count: 3
  3 3 3
  1 5 16
  3 5 15

The final output will be (for each combo above):
c
d
e

Problem 3:
==========
1.	Given a string, create as many sub strings possible.
2.	Reverse the string
3.	Find out maximum number of character that are not matching

Example1:
                Given string:                ABACC
                Reverse of the string: 	     CCABA
                Max Mismatch:            11011 = 4

Final output: 4

---
Example2:
                Given string:     ABBA
                Reverse String: ABBA
                Max Mismatch: 0000 = 0

Final output: 0


