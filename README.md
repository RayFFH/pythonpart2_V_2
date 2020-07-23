# pythonpart2_V_2
Working version for part2
import re


def add(number):
    s = int(number[0])+int(number[1])
    return s


def subtract(number):
    s = int(number[0])-int(number[1])
    return s


def multiply(number):
    s = int(number[0])*int(number[1])
    return s


def divide(number):
    s = int(number[0])/int(number[1])
    return s


calculation = input("Type your calculation")
numbers = re.findall(r'\d+', calculation)
print(numbers)

if calculation[1] == "+":
    ans = add(numbers)
    print(ans)
elif calculation[1] == "-":
    ans = subtract(numbers)
    print(ans)
elif calculation[1] == "*":
    ans = multiply(numbers)
    print(ans)
elif calculation[1] == "/":
    ans = divide(numbers)
    print(ans)
else:
    print("error")
