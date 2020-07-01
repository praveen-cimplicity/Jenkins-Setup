
WAP for Balancing of parenthesis 
# Python3 code to Check for
# balanced parentheses in an expression
open_list = ["[", "{", "("]
close_list = ["]", "}", ")"]

# Function to check parentheses
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
