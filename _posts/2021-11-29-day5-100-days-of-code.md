---
title: Day 5 of 100 days of code
categories:
- Computer science 

feature_text: |
  The journey of learning computer science by Python
---
( 2 minutes reading)

### Project: PYpassword generator!

1. what to learn: for loops, range, and code blocks
-loops: for item in list_of_items:
-loops and range function: for number in range(a,b):

2. website:
haveibeenpwned.com to check if you have an acccount have been compromised

3. Project:
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
print("Welcome to the PyPassword Generator!")
nr_letters= int(input(f"How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

password_list=[]

for char in range(1, nr_letters +1):
  password_list.append(random.choice(letters))

for char in range(1, nr_numbers +1):
  password_list.append(random.choice(numbers))

for char in range(1, nr_symbols +1):
  password_list.append(random.choice(symbols))


#print(password_list)
random.shuffle(password_list)
#print(password_list)

final=""
for char in password_list:
  final +=char
print(f"Your new password is: {final}")