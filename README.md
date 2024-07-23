# rock-paper-scissor
import random

def get_computer_choice():
    """Randomly select Rock, Paper, or Scissors for the computer."""
    choices = ['rock', 'paper', 'scissors']
    return random.choice(choices)

def determine_winner(user_choice, computer_choice):
    """Determine the winner based on the user's and computer's choices."""
    if user_choice == computer_choice:
        return 'It\'s a tie!'
    elif (user_choice == 'rock' and computer_choice == 'scissors') or \
         (user_choice == 'paper' and computer_choice == 'rock') or \
         (user_choice == 'scissors' and computer_choice == 'paper'):
        return 'You win!'
    else:
        return 'Computer wins!'

def play_game():
    """Play a single round of Rock-Paper-Scissors."""
    print("Welcome to Rock-Paper-Scissors!")
    user_choice = input("Enter Rock, Paper, or Scissors: ").strip().lower()

    if user_choice not in ['rock', 'paper', 'scissors']:
        print("Invalid choice. Please choose Rock, Paper, or Scissors.")
        return

    computer_choice = get_computer_choice()
    print(f"Computer chose: {computer_choice}")

    result = determine_winner(user_choice, computer_choice)
    print(result)

if __name__ == "__main__":
    play_game()


