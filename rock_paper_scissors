import random
import math

def play_rps():
    '''Function to get user input and computer input (based on random.choice method).
    This function also checks whether the player has won the game, lost the game or tie.'''

    user = input('What\'s your choice : \'R\' for Rock, \'P\' for Paper and \'S\' for Scissor : ').upper()
    computer = random.choice(['R', 'P', 'S'])

    if user == computer:
        return (0, user, computer)

    if wins(user, computer):
        return (1, user, computer)

    return (-1, user, computer)

def wins(player, opponent):
    '''Function to determine the logic of the game and the winning condition for both players.'''
    
    if (player == 'R' and opponent == 'S') or (player == 'S' and opponent == 'P') or (player == 'P' and opponent == 'R'):
        return True
    return False

def best_of(n):
    '''Function to check and calculate if the user has won the game out of n games.'''

    player_wins = 0
    computer_wins = 0
    wins_required = math.ceil(n/2)
    while player_wins < wins_required and computer_wins < wins_required:
        result, user, computer = play_rps()
        if result == 0:
            print(f'It\'s a Tie. You both choose {user}!')
        elif user == 1:
            player_wins += 1
            print(f'You just won the game. You choose {user} and the computer choose {computer}!')
        else:
            computer_wins += 1 
            print(f'You just lost the game. You choose {user} and the computer choose {computer}!')

    if player_wins > computer_wins:
        print(f'Congratulations. You just won out of {n} games. What a champ!')
    else:
        print(f'Sorry. You just lost the game out of {n} games. What a loser!')

if __name__ == '__main__':
    best_of(3)
