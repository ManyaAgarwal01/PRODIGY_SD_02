import random

def guess_number_game():
    print("Welcome to the Number Guessing Game!")
    print("I will pick a random number within a range you specify.")
    
    # Get the range from the user
    while True:
        try:
            lower_bound = int(input("Enter the lower bound of the range: "))
            upper_bound = int(input("Enter the upper bound of the range: "))
            
            if lower_bound >= upper_bound:
                print("Upper bound must be greater than lower bound. Please try again.")
                continue
            
            break
        
        except ValueError:
            print("Invalid input. Please enter valid integers for the bounds.")
    
    # Generate a random number within the specified range
    secret_number = random.randint(lower_bound, upper_bound)
    attempts = 0
    
    while True:
        try:
            user_guess = int(input(f"Guess the number between {lower_bound} and {upper_bound}: "))
            attempts += 1
            
            if user_guess < lower_bound or user_guess > upper_bound:
                print(f"Please enter a number between {lower_bound} and {upper_bound}.")
                continue
            
            if user_guess < secret_number:
                print("Too low! Try guessing higher.")
            elif user_guess > secret_number:
                print("Too high! Try guessing lower.")
            else:
                print(f"Congratulations! You guessed the number {secret_number} correctly!")
                print(f"It took you {attempts} attempts to win.")
                break
        
        except ValueError:
            print("Invalid input. Please enter a valid number.")

if __name__ == "__main__":
    guess_number_game()
