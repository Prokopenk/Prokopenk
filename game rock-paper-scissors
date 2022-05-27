from random import randint

def user_interface(options):
    '''
    function presenting options and asking for player feedback
    returns integer.
    '''
    for index,option in enumerate(options):
        print(f'{index} = {option}')

    user_input = int(input('What do you choose? '))
    return user_input


def computer_choice(content):
    '''
    function that generates a random number based on the available options.
    returns random int
    '''
    computer_chose = randint(0,len(content)-1)
    return computer_chose
    

def check_results(choices, player, computer):
    '''
    function that checks who won.
    returns string
    '''
    if player == computer:
        return 'It\'s a tie'
    elif (player == 0 and computer == len(choices)-1) or (player>computer and not(player==len(choices)-1 and computer==0)):
        return 'Player Won'
    return 'Player Lost'


def play():
    print('''
    ---------------------------------
    Welcome to Rock, Paper, Scissors.
    Please pick your weapon.
    ''')

    #define the options and ask contestants to pick one
    options_list = ['Rock', 'Paper' , 'Scissors']
    player_result = user_interface(options_list)
    computer_result = computer_choice(options_list)
    
    #viusual representation in the terminal so we can see what both parties chose
    print(f'  player chose: {options_list[player_result]}')
    print(f'computer chose: {options_list[computer_result]}')

    #check the results between the two and print the winner.
    results = check_results(options_list,player_result,computer_result)
    print (f'\n{results}')

def main():

    #force the player into the play loop
    play_again = ''
    while play_again.lower() != 'n':
        play()
        print (f'Do you want to play again? ')
        play_again = input('type \'y\' for yes or \'n\' for no: ')

main()
