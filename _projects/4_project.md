---
layout: page
title: Simple Python projects
description: another without an image
img: assets/img/turkeys.jpg
importance: 3
category: fun
---

This code was made just for fun and when I started learning Python. The Turkeys' picture has nothing to do with the theme of this project, but I like it!

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/turkeys.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

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
