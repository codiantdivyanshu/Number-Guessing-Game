import random


secret_number = random.randint(1, 100)


guess = None
tries = 0

print(" Welcome to the Number Guessing Game!")
print("I'm thinking of a number between 1 and 100...")

while guess != secret_number:
    try:
        guess = int(input("Enter your guess: "))
        tries += 1

        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print(f"Correct! You guessed the number in {tries} tries.")
    except ValueError:
        print(" Please enter a valid number.")
