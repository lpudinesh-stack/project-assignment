# project-assignment
this project is related to my assignment 
import random

choices = ["rock", "paper", "scissors"]

while True:
    user = input("Enter rock, paper, or scissors (or quit): ").lower()

    if user == "quit":
        print("Game ended.")
        break

    if user not in choices:
        print("Invalid choice. Try again.")
        continue

    cpu = random.choice(choices)

    print("You:", user)
    print("Computer:", cpu)

    if user == cpu:
        print("Result: Tie\n")
    elif (user == "rock" and cpu == "scissors") \
        or (user == "paper" and cpu == "rock") \
        or (user == "scissors" and cpu == "paper"):
        print("You win!\n")
    else:
        print("Computer wins!\n")
  
