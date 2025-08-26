# Python-programming-game
# A simple implementation of the classic Rock Paper Scissors game in Python. This interactive game allows users to play against the computer, with random computer choices and tracking of wins, losses, and ties. Users can continue playing, view the final score, or exit the game.
import random

def play_game():
    choices = [“rock”, “paper”, “scissors”]
    user_wins = 0
    computer_wins = 0
    matches = 0
    tie_round = 0

    while True:
        user_choice = input(“Enter your choice (rock, paper, or scissors): “)

        if user_choice not in choices:
            print(“You choose an invalid choice! Please choose rock, paper, or scissors.”)
            continue        

        computer_choice = random.choice(choices)
        print(f”You choose:{user_choice}”)
        print(f”computer choose:{computer_choice}”)
        matches += 1

        if user_choice == computer_choice:
            print(“This round is a tie!”)
            tie_round += 1
        elif (user_choice == “rock” and computer_choice == “scissor”) or \
             (user_choice == “paper” and computer_choice == “rock”) or \
             (user_choice == “scissor” and computer_choice == “paper”):
            print(“You win this round!”)
            user_wins += 1
        else:
            print(“computer wins this round!”)
            computer_wins += 1

print()

         while True:
            opt = input(“Enter 1 to Continue, 2 to see Final Score, 3 to Exit: “)
            If opt == ‘1’:
                break 
            elif opt == ‘2’:
                print(f”\nFinal Score – matches: {matches}, You: {user_wins}, computer: {computer_wins}, tie: {tie_round}”)
                if user_wins > computer_wins:
                    print(“You won more rounds!”)
                elif user_wins < computer_wins:      
            print(“computer won more rounds!”)
                else:
                    print(“It was a tie in total wins!”)                                elif opt == '3' print(“Exiting game.”)

                return

            elif opt != ‘1’:

                print(“Invalid option. Please enter 1, 2, or 3.”)

play_game()

