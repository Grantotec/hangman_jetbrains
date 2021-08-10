from random import choice


print('H A N G M A N')
words = ('python', 'java', 'kotlin', 'javascript')

command = input('Type "play" to play the game, "exit" to quit:')


while command not in ['play', 'exit']:
    print("Let's thinking better")
    command = input('Type "play" to play the game, "exit" to quit:')


while command == 'play':
    our_choice = choice(words)
    word = list(our_choice)
    hint = list('-' * len(word))
    lives = 8
    letters = set()
    while lives != 0 and '-' in hint:
        print('')
        print(''.join(hint))
        letter = input('Input a letter:')
        if len(letter) != 1:
            print('You should input a single letter')
            continue
        if ord(letter) < 97 or ord(letter) > 122:
            print('Please enter a lowercase English letter')
            continue
        if letter in letters:
            print("You've already guessed this letter")
            continue
        letters.add(letter)
        if letter in word:
            for i in range(len(hint)):
                if word[i] == letter:
                    hint[i] = word[i]
        else:
            print("That letter doesn't appear in the word")
            lives -= 1
    if lives == 0:
        print('You lost!')
    else:
        print("\n{}\nYou guessed the word!\nYou survived!".format(our_choice))
    command = input('\nType "play" to play the game, "exit" to quit:')
else:
    quit()
