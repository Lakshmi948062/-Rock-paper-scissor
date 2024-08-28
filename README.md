import random
def get_computer_choice():
  choices=["rock","paper","scissors"]
  return random.choice(choices)

def get_user_choice():
  user_choice=input("Enter rock,paper,or scissors").lower()
  while user_choice not in["rock","paper","scissors"]:
    print("Invalid choice please do enter the choice again.")
    user_choice=input("Enter rock,paper,or scissors").lower()
  return user_choice

def determine_winner(user_choice,computer_choice):
  if user_choice==computer_choice:
    return "Its is a tie"

  if (user_choice=="rock" and computer_choice=="scissors") or \
     (user_choice=="scissors" and computer_choice=="rock") or \
     (user_choice=="paper" and computer_choice=="rock"):
     return "you win"

  return "computer win"

def play_game():
  print("welcome to the ROCK PAPER SCISSORS game")
  user_choice=get_user_choice()
  computer_choice=get_computer_choice()

  print(f"you choose:{user_choice}")
  print(f"computer_choice:{computer_choice}")

  result=determine_winner(user_choice,computer_choice)
  print(result)

play_game()
