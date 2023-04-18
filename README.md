# Python-Program-to-Finding-out-the-Prime-Factors-of-a-Number

Find the Prime Factors of a Number in Python
Given an integer input as the number, the objective is to Find all the Prime Factors of a the given integer input number. Therefore, we’ll write a program to Find the Prime Factors of a Number in Python Language.

Example
Input : 10
Output : 2 5
Prime Factors of a Number in Python
Find the Prime Factors of a Number in Python Language
Given an integer input as the number, the objective is to find all the prime factors of a Number in Python Language. To do so, we’ll first find all the factors of a Number, meanwhile check whether the number is a Prime or not. If a Number is Even, it’ll has 2 as it’s prime factor. Here are some of the methods we’ll use to solve the above mentioned problem,

Method 1: Using Simple Iteration
Method 2: Using Recursive Function
We’ll discuss the above mentioned methods in detail in the up coming sections. To know how to check for prime, check out our page, Find Whether or Not the Number is a Prime. Don’t forget to check the blue box below for better understanding of the problem.


Method 1: Using Simple Iteration
Working
In this method we’ll use the concept of loops to find all the factors of a number and to check whether or not the number is a Prime or not. We’ll iterate through numbers in a given range and check if the number is divisible by the numbers or not.

Given an integer input as a number, We’ll perform the following,

Run a while loop with condition n>1.
Run a nested for loop until (2+n//2).
if i == ( 1+ n//2), append the n value and shorten the number by n = n//n.
if n%1==0, append the i value and short the n as n= n//i.
Return the array and print it.
Let’s implement the above mentioned logic in Python Language.

Python Code
Run
def Prime_Factorial(n):
    if n < 4:
        return n
    arr = []
    while n > 1:
        for i in range(2, int(2+n//2)):
            if i == (1 + n // 2):
                arr.append(n)
                n = n // n
            if n % i == 0:
                arr.append(i)
                n = n // i
                break
    return arr


n = 210
print(Prime_Factorial(n))
Output
[ 2 , 3 , 5 , 7 ]
Related Pages
Power of a number

Factor of a number

Finding Prime Factors of a number

Strong number

Perfect number

Perfect Square

Method 2: Using Recursive Function
Working
In this method we’ll use recursion to recursively find the factors and check whether they are prime or not. To do so we’ll create a recursive function and recursively check for factors that are prime.

For an integer input, we perform the following,

Define a recursive function, Prime_factorial() which takes the number and the output array as arguments.
Set the base case as number<4 and step recursive call as Prime_Factorial(number//iter , output_arr).
Return the output array and print it.
Let’s implement the above mentioned logic in Python Language. To know more about recursion in Python, check out our page Recursion in Python.

Python Code
Run
def Prime_Factorial(n, arr):
    if n < 4:
        return n
    for i in range(2, int(2+n//2)):
        if i == (1 + n // 2):
            arr.append(n)
            n = 1
            return
        if n % i == 0:
            arr.append(i)
            n = n // i
            Prime_Factorial(n, arr)
            break
    return arr


n = 210
arr = []
print(Prime_Factorial(n, arr))
Output
[ 2, 3, 5, 7 ]
