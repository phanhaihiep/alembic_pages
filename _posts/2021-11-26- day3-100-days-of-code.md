---
title: Day 3 of 100 days of code
categories:
- Computer science 

feature_text: |
  The journey of learning computer science by Python
---
( 2 minutes reading)

### Project: GAME: Tresure Island

1. what to learn: Condition statment, Logical operators, code blocks and scope
- if/else condition have 3 kinds:
    + if condition:   
        do this
      else:
        do this
    + if condition with more condition if elif  
        if another condition:
          do A
        elif another condition 2:
          do B
        else:
          do this
      else:
        do this
    + if condition with mutilple if
      if condition 1:
        do A
      if conditiion 2:
        do B
      if condition 3:
        do C
    + if condition 1 & condition 2 & condition 3:
        do this
      else:
        do that
- modulo sign % for example 7/3 = 1 (reason 3+3+1) you get remainder 1
- name =name.lower()
- name =name.count()

2. tools:
- draw.io
- (https://ascii.co.uk/art): You can also add your own ASCII art(https://ascii.co.uk/art). Just remember to add three single quotes ''' at the start and at the end of your artwork to turn it into a multi-line string. 

3. projects: GAME TREASURE ISLAND
https://replit.com/@HiepPhan/treasure-island-start?v=1

  print('You\'re at a crossroad. Where do you want to go? Type "left" or "right".\n')

  game1=input().lower()
  if game1=="left":
    print('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.\n')
  else:
    print("Fall into a hole. Game over")

  game2=input().lower()
  if game2=="swim":
      print("You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?\n")  
  else:
      "You get attacked by an angry trout. Game Over."

  game3=input().lower()
  if game3=="yellow":
    print("You found the treasure! You Win!")
  elif game3=="blue":
    print("You enter a room of beasts. Game Over.")
  elif game3=="red":
    print("It's a room full of fire. Game Over.")
  else:
    print("You chose a door that doesn't exist. Game Over.")

4. note
-using the back slash: You\'re: when you have both "" and '', you need a back slash to understand the 're
-using the function .lower() to make sure all the input are converted in to small letters.
-using the \n after the . for the enter a new sentence