# Python-Project
import random

lowest_num = 1
highest_num = 100
answer = random.randint (lowest_num, highest_num )
guesses = 0
is_running =True

print("Python Number Guessing Game!")
print(f"Select the number between {lowest_num} and {highest_num}")

while is_running:
     
     guess = input("Enter your guess:")

     if guess.isdigit():
        guess = int(guess)
        guesses +=1

        if guess < lowest_num or guess > highest_num:
            print("That number is out of range.")
            print(f"Please select between our {lowest_num} and {highest_num}")
        elif guess < answer:
            print("Too Low! Try again")
        elif guess > answer:    
            print("Too High! Try again")
        else:
            print(f"CORRECT! The answer was : {answer}")
            print(f"Number of guesses: {guesses}")
            is_running= False

        pass
     else:
         print("Invalid Guess")
         print(f"Please select between our {lowest_num} and {highest_num}")
