---
title: Day 2 of 100 days of code
categories:
- Computer science 

feature_text: |
  The journey of learning computer science by Python
---
( 2 minutes reading)

### Project: TIP CALCULATOR

1. what to learn
- data types: string, float, interger, boolean
  + string: print("Hello"[1])
  + interger: 123456
  + float: 31.50
  + Boolean: True or False
- function is like a machine to process the ingredient which is data
- to check a type of data using: type()
- convert a data type using: new_num_char = str(num_char)
- convert a number like 1.0 to 1 by using int(1.0)
- mathematic operation in python: PEMDAS () ** * / + -
- using round() function to round a number up or down: round(2.6666 , 2)
- using // to divide int number 8//3 = 2
- score = score + 1, another short way is score += 1
- f-string: print(f"your score is {score}, your height is {height}, your IBM value is {IBM}"): this one we dont have to put datatype infont of each data. All diffrent data type are converted into string.
- to round the 2 numbers we can use the format: final_amount = "{:.2f}".format(bill_person)

2. Project
#If the bill was $150.00, split between 5 people, with 12% tip. 
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
#Write your code below this line 👇
print("Welcome to the tip calculator!")
bills = float(input("What was the total bill?$"))

tips = int(input("How much tip would you like to give?"))

no_pp = int(input("How many people to split the bill?"))

sum_bills = bills/no_pp*(1+(tips/100))

pay=round(sum_bills, 2)

print(f"Each person should pay: {pay}")

https://replit.com/@HiepPhan/tip-calculator-start?v=1
