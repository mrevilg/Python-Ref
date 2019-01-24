### Rock Paper Scissors
#1 Long winded

  ```python 
  import random

  random_choice = random.randint(0,2)

  if random_choice == 0:
      computer_choice = 'rock'
  elif random_choice == 1:
      computer_choice = 'paper'
  else:
      computer_choice = 'scissors'

  user_choice = input('rock, paper or scissors? ')

  print('You chose', user_choice, 'and the computer chose', computer_choice)
  ```
  
#2 Given choices

  ```python
  import random

  choices = ['rock', 'paper', 'scissors']
  computer_choice = random.choice(choices)

  user_choice = input('rock, paper or scissors? ')

  print('You chose', user_choice, 'and the computer chose', computer_choice)
  ```
