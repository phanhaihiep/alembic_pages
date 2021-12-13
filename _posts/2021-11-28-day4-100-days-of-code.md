---
title: Day 4 of 100 days of code
categories:
- Computer science 

feature_text: |
  The journey of learning computer science by Python
---
( 2 minutes reading)

### Project: ROCK PAPER SCISSORS GAME

1. what to learn: randomisation and python lists.
import random
random_number = random.randint(100,200)--- generate the interger number
print(random_number)

random_number = random.random()--- generate the float number from 0 to 1
print(random_number)

if you want a range from 0 to 5, you can multiple for 5.
random_number *5 
print(random_number)

python lists: is data structure, a way to organize and store data in python
for example: fruits=[item1, item2] or fruits=["cherry", "apple", "pear"]
list always start with square bracket [] seperate by comma
you can querry the order from the list using print(fruit[0]) for the first position or print(fruits[-1]) for the last position
you can change the value of the list using fruits[1]="orange" then new list is fruits=["cherry", "orange", "pear"]
you can add 1 value of the list using append fruits.append("banana") then new list is fruits=["cherry", "orange", "pear", "banana"]
you can add more than 1 value using extend fruits.extend(["kiwi","mango"])
you can use function random.choice(a) in list a to pick 1 value
note, be mindful with list to start with 0, so list-1 when using random
conver string to list names = names_string.split(", ")
list contains 2 lists, you will see 2 brackets [[]]

2. Project:
+++ My code:
import random
list_game=["rock", "paper", "scissors"]
player= input("What is your choice? type 1 for rock or 2 for paper or 3 for scissors?\n ")

game = random.choice(list_game)
print(f"Computer choose: {game}")

if player == "rock" and game == "rock":
  print("Equal")
elif player == "paper" and game =="paper":
  print("Equal")
elif player ==  "scissors" and game == "scissors":
  print("Equal")

elif player ==  "scissors" and game == "rock":
  print("Computer wins, you lose")
elif player ==  "rock" and game == "scissors":
  print("You win, computer loses")

elif player ==  "rock" and game == "paper":
  print("Computer wins, you lose")
elif player ==  "paper" and game == "rock":
  print("You win, computer loses")

elif player ==  "scissors" and game == "paper":
  print("You wins, computer loses")
elif player ==  "paper" and game == "scissors":
  print("Computer wins, you lose")

else:
  print("game on")

  +++ My improve code:
import random

list_game=[rock, paper, scissors]

player= int(input("What is your choice? type 0 for rock or 1 for paper or 2 for scissors?\n"))
if player >= 3 or player < 0:
  print("You input an invalid number, you lose") 

else:
  print(list_game[player])
  game = random.randint(0, 2)
  print("Computer chose:")
  print(list_game[game])

  if player == 0 and game == 2:
    print("You wins!")
  elif player == 2 and game == 0:
    print("You lose!")
  elif player > game:
    print("You win!")
  elif player == game:
    print("It's a draw")
  elif player < game:
    print("You lose!"))

