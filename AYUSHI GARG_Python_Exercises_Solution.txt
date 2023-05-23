#QUESTION 1

a = 21
b = 6
c = 3
d = 1
print(a - b / c)
print((a - b) / c)
print(a/b*c+d)
print(a/(b*(c+d)))



#QUESTION 2

import sys
a = float(sys.argv[1])
b = float(sys.argv[2])
c = float(sys.argv[3])
d = float(sys.argv[4])
e = float(sys.argv[5])
a += 1
print(a)
print(a+1)
a += 1
b = b + 1
c = c + 1
print((a + b) / c)
d = d + 1
print(a / (b * (c + d)))
b = b + 1
c = c + 1
d = d - 1
e = e - 1
print(a ** b + b ** c + c ** d + d ** e)



#QUESTION 3

a = 2.5  # float
b = 3.14159  # double
c = 120  # byte
d = 32000  # short
e = 5000000000  # long
short result = short(e)
short result_2 = short(c - e)
short result_3 = short(e - a)

# Type cast long to int
short result_4 = int(e)

# Type cast int to short
short result_5 = short(d)

# Type cast double to float
short result_6 = float(b)

# Type cast float to byte
short result_7 = byte(a)

# Type cast int to long
short result_8 = long(d)

# Type cast short to long
short result_9 = long(d)

# Type cast float to double
short result_10 = double(a)

# Type cast byte to float
short result_11 = float(c)



#QUESTION 4

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
op = input("Enter operation to be carried out (a = addition, s = subtraction, m = multiplication, d = division): ")
result = 0.0
if op == 'a':
    result = num1 + num2
elif op == 's':
    result = num1 - num2
elif op == 'm':
    result = num1 * num2
elif op == 'd':
    if num2 == 0:
        print("Error: division by zero")
    else:
        result = num1 / num2
else:
    print("Error: invalid operation")
print("Result:", result)




#QUESTION 5

import math
while True:
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    op = input("Enter operation to be carried out (a = addition, s = subtraction, m = multiplication, d = division, p = power, e = exponentiation, mod = modulo operator, sin = sine, cos = cosine, tan = tangent): ")

    if op == 'a':
        result = num1 + num2
    elif op == 's':
        result = num1 - num2
    elif op == 'm':
        result = num1 * num2
    elif op == 'd':
        result = num1 / num2
    elif op == 'p':
        result = num1 ** num2
    elif op == 'e':
        result = math.exp(num1)
    elif op == 'mod':
        result = num1 % num2
    elif op == 'sin':
        result = math.sin(num1)
    elif op == 'cos':
        result = math.cos(num1)
    elif op == 'tan':
        result = math.tan(num1)
    else:
        print("Invalid operation selected")
        continue

    print("Result:", result)
    choice = input("Do you want to continue (y/n)? ")
    if choice == 'n':
        break



#QUESTION 6

def factorial(n):
    fact = 1
    for i in range(1, n+1):
        fact *= i
    return fact
n = int(input("enter the number:"))
print(f"{n}! = {factorial(n)}")



#QUESTION 7a

for i in range(1, 9):
    for j in range(1, 2):
        print("* ", end="")
    print(end=" ")



#QUESTION 7b

for i in range(1, 6):
    for j in range(1, 9):
        if i == 1 or i == 5 or j == 1 or j == 8:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()



#QUESTION 7c

height = 8
# Print the shape using nested for loops
for i in range(1, height+1):
    for j in range(1, i+1):
        if i == height or j == 1 or j == i:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()



#QUESTION 7d

rows = 7
for i in range(rows):
    for j in range(rows-i-1):
        print(" ", end="")
    if i == 0:
        print("*")
    else:
        print("*", end="")
        for k in range(2*i-1):
            print(" ", end="")
        print("*")
for i in range(rows):
    print("* ", end="")
print()



#QUESTION 8

arr = []
for i in range(10):
    num = int(input(f"Enter number {i+1}: "))
    arr.append(num)
sum = 0
for num in arr:
    sum += num
avg = sum / len(arr)
print("Array:", arr)
print("Average:", avg)



#QUESTION 9

arr = []
for i in range(10):
    num = int(input(f"Enter number {i+1}: "))
    arr.append(num)
arr.sort()
print("Sorted (ascending) array:", arr)
arr.reverse()
print("Sorted (descending) array:", arr)



#QUESTION 10

arr = []
for i in range(10):
    num = int(input(f"Enter element {i+1}: "))
    arr.append(num)
search = int(input("Enter the element to search: "))
found = False
for num in arr:
    if num == search:
        found = True
        break
if found:
    print(f"Element {search} found in the array")
else:
    print(f"Element {search} not found in the array")



#QUESTION 11

name = input("Enter a name: ")
reverse_name = name[::-1]
if name.lower() == reverse_name.lower():
    print(f"{name} is a palindrome!")
else:
    print(f"{name} is not a palindrome.")



#QUESTION 12

def is_equal(arr1, arr2):
    if len(arr1) != len(arr2):
        return False
    arr1 = sorted(arr1)
    arr2 = sorted(arr2)   
    for i in range(len(arr1)):
        if arr1[i] != arr2[i]:
            return False
    return True
def is_identical(arr1, arr2):
    if len(arr1) != len(arr2):
        return False
    for i in range(len(arr1)):
        if arr1[i] != arr2[i]:
            return False
    return True
arr1 = [1, 2, 3, 4, 5]
arr2 = [5, 4, 3, 2, 1]
if is_equal(arr1, arr2):
    print("The arrays are equal (irrespective of position).")
else:
    print("The arrays are not equal (irrespective of position).")
if is_identical(arr1, arr2):
    print("The arrays are identical (taking position into account).")
else:
    print("The arrays are not identical (taking position into account).")



#QUESTION 13

import random
arr = [random.randint(0, 99) for _ in range(100)]
print(arr)



#QUESTION 14

import random
arr = [random.randint(0, 99) for _ in range(100)]
print("Original array:", arr)
arr_without_duplicates = list(set(arr))
print("Array without duplicates:", arr_without_duplicates)



#QUESTION 15

class Stack:
    def __init__(self):
        self.items = []    
    def is_empty(self):
        return len(self.items) == 0 
    def push(self, item):
        self.items.append(item)
    def pop(self):
        if self.is_empty():
            return None
        else:
            return self.items.pop()
    def peek(self):
        if self.is_empty():
            return None
        else:
            return self.items[-1]
    def size(self):
        return len(self.items)
stack = Stack()
stack.push(1)
stack.push(2)
stack.push(3)
print(stack.peek())   
print(stack.pop())    
print(stack.pop())    
print(stack.size())   
print(stack.is_empty())  



#QUESTION 16 

class Queue:
    def __init__(self):
        self.items = []
    def is_empty(self):
        return self.items == []
    def enqueue(self, item):
        self.items.append(item)
    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
    def size(self):
        return len(self.items)
q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
print(q.dequeue())  
print(q.dequeue())  
print(q.size())    



















