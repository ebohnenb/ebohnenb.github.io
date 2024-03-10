---
layout: page
title: Simple Python projects
description: Simple coding projects to learn and practice Python.
img: assets/img/turkeys.jpg
importance: 3
category: fun
---

Project 1 : Rock-Scissor-Paper game. Your computer and you!!

   {% raw %}
```
import random

def rps(y):
    game_dict= {1: 'rocks', 2:'paper', 3:'scissors'}
    x = random.choice([1, 2, 3])
    outcome = y - x

    feedback = f'You played {game_dict.get(y)}, the computer played {game_dict.get(x)}.'

    if outcome in [-2, 1]:
        print(f'{feedback}\nYou win!')
    elif outcome in [-1, 2]:
        print(f'{feedback}\nComputer win!.')
    else:
        print(f'{feedback}\nIt\'s a tie!')

def play_again():
    try:
        again = input('Would you like to play again (y)es or (n)o? ')

        if again not in ['y', 'n']:
            raise ValueError
    
    except Exception:
        print('\nError: wrong input!')
        play_again()

    else:
        if again == 'y':
            main ()
        else:
            print('Good bye!')


def main():
    try:
        y= int(input(' Choose (1) for rocks, (2) for paper, or (3) for scissors: '))

        if y <1 or y > 3:
            raise ValueError

    except ValueError:
        print('\nERROR: wrong input!!! Try again.')
        main()

    else:
        rps(y)

    finally:
        play_again()


if __name__== '__main__':
    pass

import rps
rps.main()
```
{% endraw %}

----------------------------------

Project 2 : 

