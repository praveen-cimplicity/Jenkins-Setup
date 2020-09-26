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

##Demonstrate Pickling and unpickling
Pickling happens when a module within Python is accepted and converted into a string
module, and then later dumped into the file.
As opposed to that, unpickling is when you retrieve the string module from the file.
For such comparison-based Python interview questions, try to keep your explanations as simple
as possible. Your potential employers will probably appreciate that you are able to explain tough
topics in a simple-to-understand manner.

######
LOG PARSER
######
def get_next_event(filename):
    with open(filename, "r") as datafile:
        for line in datafile:
            if "dut: Device State: " in line:
                line = line.strip()
                # Parse out the action and timestamp
                action = line.split()[-1]
                timestamp = line[:19]
                yield (action, timestamp)


Q1: What are virtualenvs? What are virtualenvs?
96 Python Interview Questions  Python  96  Mid
Answer
A virtualenv is what Python developers call an isolated environment for development, running, debugging Python code. It is used to isolate a Python interpreter together with a set of libraries and settings. Together with pip, it allows us to develop, deploy and run multiple applications on a single host, each with their own version of the Python interpreter, and separate set of libraries.

Interview Coming Up?  Check 96 Python Interview Questions
linkadevait.com
Q2: What is the python “with” statement designed for? What is the python “with” statement designed for?
96 Python Interview Questions  Python  96  Mid
Answer
The with statement simplifies exception handling by encapsulating common preparation and cleanup tasks in so-called context managers.

For instance, the open statement is a context manager in itself, which lets you open a file, keep it open as long as the execution is in the context of the with statement where you used it, and close it as soon as you leave the context, no matter whether you have left it because of an exception or during regular control flow.

As a result you could do something like:

with open("foo.txt") as foo_file:
    data = foo_file.read()
OR

from contextlib import nested
with nested(A(), B(), C()) as(X, Y, Z):
    do_something()
OR (Python 3.1)

with open('data') as input_file, open('result', 'w') as output_file:
    for line in input_file:
        output_file.write(parse(line))
OR

lock = threading.Lock()
with lock: #Critical section of code
Interview Coming Up?  Check 96 Python Interview Questions
linkstackoverflow.com
Q3: What is the function of “self”? What is the function of “self”?
96 Python Interview Questions  Python  96  Mid
Answer
Self is a variable that represents the instance of the object to itself. In most of the object oriented programming language, this is passed to the methods as a hidden parameters that is defined by an object. But, in python, it is declared and passed explicitly. It is the first argument that gets created in the instance of the class A and the parameters to the methods are passed automatically. It refers to separate instance of the variable for individual objects.

Let's say you have a class ClassA which contains a method methodA defined as:

def methodA(self, arg1, arg2): #do something
and ObjectA is an instance of this class.

Now when ObjectA.methodA(arg1, arg2) is called, python internally converts it for you as:

ClassA.methodA(ObjectA, arg1, arg2)
The self variable refers to the object itself.


Q4: What does the Python nonlocal statement do (in Python 3.0 and later)? What does the Python nonlocal statement do (in Python 3.0 and later)?
Answer
In short, it lets you assign values to a variable in an outer (but non-global) scope.

The nonlocal statement causes the listed identifiers to refer to previously bound variables in the nearest enclosing scope excluding globals.

For example the counter generator can be rewritten to use this so that it looks more like the idioms of languages with closures.

def make_counter():
    count = 0
    def counter():
        nonlocal count
        count += 1
        return count
    return counter
    

Q5: What are the wheels and eggs? What is the difference? What are the wheels and eggs? What is the difference?
Wheel and Egg are both packaging formats that aim to support the use case of needing an install artifact that doesn’t require building or compilation, which can be costly in testing and production workflows.

The Egg format was introduced by setuptools in 2004, whereas the Wheel format was introduced by PEP 427 in 2012.

Wheel is currently considered the standard for built and binary packaging for Python.

Here’s a breakdown of the important differences between Wheel and Egg.

Wheel has an official PEP. Egg did not.
Wheel is a distribution format, i.e a packaging format. 1 Egg was both a distribution format and a runtime installation format (if left zipped), and was designed to be importable.
Wheel archives do not include .pyc files. Therefore, when the distribution only contains Python files (i.e. no compiled extensions), and is compatible with Python 2 and 3, it’s possible for a wheel to be “universal”, similar to an sdist.
Wheel uses PEP376-compliant .dist-info directories. Egg used .egg-info.
Wheel has a richer file naming convention. A single wheel archive can indicate its compatibility with a number of Python language versions and implementations, ABIs, and system architectures.
Wheel is versioned. Every wheel file contains the version of the wheel specification and the implementation that packaged it.
Wheel is internally organized by sysconfig path type, therefore making it easier to convert to other formats.

Q6: What are metaclasses in Python? What are metaclasses in Python?
Answer
>>

#MongoDB   #NoSQL   #SQL  
Q7: How to make a chain of function decorators? How to make a chain of function decorators?
96 Python Interview Questions  Python  96  Senior
Details
How can I make two decorators in Python that would do the following?

@makebold
@makeitalic
def say():
   return "Hello"
which should return:

"<b><i>Hello</i></b>"
Answer



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

===============
[AUTH TOKEN]
3 test cases for api testing token authenticate which run in parallel from different remote machines. 
Tc1 - (which runs for 2 min provided valid token exists)
Tc2 - (which runs for 3 min provided valid token exists)
Tc3 - (which runs for 4 min provided valid token exists)
 
Due to token expiry duration being changed to 2 min in the environment, it terminates the rest of the test cases. How to overcome this?

Possible workaround: Store the token in jenkins env var or in a file and run a timer to fetch valid token before expiry so the valid token is always present until last TC is executed.

[Jenkins API]

import json
import requests
import time



job_name = "testjob"   #Give your job name here


def jenkins_job_status(job_name):
        
        try:
                url  = "https://your_jenkins_endpoint/job/%s/lastBuild/api/json" %job_name   #Replace 'your_jenkins_endpoint' with your Jenkins URL
                while True:
                        data = requests.get(url).json()
                        if data['building']:
                                time.sleep(60)
                        else:
                                if data['result'] == "SUCCESS":

                                        print "Job is success"
                                        return True
                                else:
                                        print "Job status failed"
                                        return False

                
        except Exception as e:
                print str(e)
                return False




if __name__ == "__main__":

        if jenkins_job_status(job_name):

                print "Put your autmation here for 'job is success' condition"

        else:
                print "Put your autmation here for 'job is failed' condition"                
	



Demonstrate HTTP GET example:

import requests
import json
import jsonpath

url = 'https://reqres.in/api/users?page=1' #string variable'

#send get requests

response = requests.get(url)  # Request to the server, will get some response from server and store it into response

print(response)  # Print the response whatever response will get from the server

print(response.content)  # it will give content of the response


json_response = json.loads(response.text)  #parse response to json format,whatever response getting just loading into the Json format

print(json_response)

for each in json_response['data']:
            print(each['email'])
            assert (each['email']) == (each['first_name']).lower()+"."+(each['last_name']).lower()+"@reqres.in"
            #assert (each['email']) == (each['first_name']).lower()+"."+(each['last_name']).lower()+"@reqrest.in"



#fetch any specific value using Jsonpath

Page=jsonpath.jsonpath(json_response,'total_pages') # it will store in list formate
#assert Page[0] == 1
assert Page[0] == 2






 
Demonstrate HTTP PUT Example:
import requests
import json
import jsonpath

# Below is a sample json
# Nested structure

#{"fields":{"summary":"[Dummy | Radar to Jira Tool Test Issue]Request to install couple of plugins needed for Xray Demo in RNO Jenkins","issuetype":{"name":"Task"},"customfield_10303":{"name":"Task"},"customfield_11402":1598940878048,"project":{"key":"TESDEV"},"description":"Hi Arun,\n\nCould you please help us with a Radar request for installing below plugins in PROD Jenkins instance?\n\n1. XRAY Connector plugin - <https://updates.jenkins-ci.org/download/plugins/xray-connector> \n2. Jira Trigger Plugin: <https://updates.jenkins.io/download/plugins/jira-trigger>\n\nThanks!\nnull\n","customfield_11401":1587031546000}}



url = 'https://reqres.in/api/users'

file = open("CreatePostRequest.json",'r')
json_input = file.read()  #reading the file content (content in string format ) and storeing into variable

request_json = json.loads(json_input)  #import json module
                                        # .loads()  convert string format to json format
#print(request_json)  # request_json contain json body

#post request with json input body
response = requests.post(url,request_json)
print("my content is", response.content)
assert response.status_code == 201  #validate response code

print('my header response ',response.headers.get('Content-Type')) #get header from response

#Parse response  (response : text format to json format)

response_json = json.loads(response.text)
id = jsonpath.jsonpath(response_json,'id')  #id will store in list
print(id[0])  #first occurance for evry time it will give random value
response = requests.get(url)
print(response.content)


CreatePostRequest.json

{
    "name": "Shanthi",
    "job": "QA"
}


