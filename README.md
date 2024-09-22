# rock-paper-scissors-game-by-using-python
import random

def play_rps():
    # Available choices
    choices = ['rock', 'paper', 'scissors']
    
    # Mapping for win conditions
    win_conditions = {
        'rock': 'scissors',
        'scissors': 'paper',
        'paper': 'rock'
    }
    
    # Get user choice
    user_choice = input("Choose rock, paper, or scissors: ").lower()
    
    # Validate user choice
    if user_choice not in choices:
        print("Invalid choice! Please choose either rock, paper, or scissors.")
        return
    
    # Get computer's random choice
    computer_choice = random.choice(choices)
    
    print(f"Computer chose: {computer_choice}")
    
    # Determine the winner
    if user_choice == computer_choice:
        print("It's a tie!")
    elif win_conditions[user_choice] == computer_choice:
        print("You win!")
    else:
        print("You lose!")

# Start the game
play_rps()
