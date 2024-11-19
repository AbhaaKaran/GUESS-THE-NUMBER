# GUESS-THE-NUMBER
import random

def guess_the_number():
    print("Welcome to 'Guess the Number'!")
    print("I'm thinking of a number between 1 and 100.")
    print("Try to guess it in as few attempts as possible!")

    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guessed_correctly = False

    while not guessed_correctly:
        guess = input("Enter your guess: ")
        
        # Check if the input is a valid number
        if not guess.isdigit():
            print("Invalid input! Please enter a number.")
        else:
            guess = int(guess)
            attempts += 1
            
            # Compare the guess to the target number
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed it in {attempts} attempts.")
                guessed_correctly = True

    guess_the_number()
