#!/usr/bin/env python3

# this will import from Google Text-To-Speech. which will allow text output to be converted into an audio file.
from gtts import gTTS
import os

# This will give the output a random argument
import random

when = ['Once upon a time, ']

# an
who = ['adventurer']

# named
name = ['Timmy']

# went to the
went = ['skate park', 'carnival', 'mall', 'pond', 'art gallery','zoo', 'gym', 'bank', 'hospital', 'Nickelback concert',
        'block party', 'football game', 'mountain', 'beach', 'candy shop', 'library', 'hospital', 'Nickelback concert']

# to find
why = ['a job, ', 'friends, ', ' a can of soda, ', 'a tutor, ', 'a mentor, ', 'breakfast, ', 'friends, ',
       'a little joy, ', 'a musical instrument, ', 'a priest, ', 'a stick of butter, ', 'a mentor, ', 'breakfast, '] 

# but instead, found a
happened = ['wallet.', 'spoon.', 'shoe.', 'cave.', 'cat.', 'leopard.', 'panda.', 'bumper sticker.', 'honda accord.',
            'weird looking man.', 'mirror.', 'shoe.', 'cave.', 'cat.', 'sock.', 'chicken coop.', 'pencil.']

# Suddenly,
speechless = [' A cave dweller', ' Harry Potter', ' Homer Simpson', ' Gordon Ramsey', ' Captain America',
              ' Dwayne Johnson', ' Rick Sanchez', ' Elon Musk', ' A little old man', ' Peter Griffin', ' Florida Man']

# appeared, holding a
appeared = [' frying pan!', ' cookie!', ' gatorade!', ' spoon!', ' plastic bag!',
            ' baby!', ' will!', ' fork!', ' knife!', ' letter!', ' pool stick!', ' book!',
            ' head of lettuce!', ' carrot!', ' tie!', ' brownie!', ' basket!',
            ' snack!', ' microphone!', ' fish!', ' Nintendo Switch!']

# Then, he
then = [' spoke ever so softly.', ' started panicking.', ' remained calm.', ' started singing.',
        ' started rapping until the adventurer complimented his skills.', ' gracefully slipped on a banana.',
        ' started complimenting everything around him.', ' started to cry.', ' pondered for a moment...']

# "I have a quest for you, young adventurer. I need you to bring me a

need = [' random letter."', ' pickle."', ' soda."', ' t-shirt."', ' little bit of water."', ' waffle."', ' pizza."',
        ' Redbull."', ' clock."', ' dog."', ' bowl of cereal."', ' helicopter."', ' million dollars."', ' sandwich."']

# Timmy obliged, vowing to accomplish the task.

# A few days later, the adventurer realized

realized = [' he was hungry.', ' his car insurance has expired.', ' he forgot to call his mother.',
            ' it was all a game.', ' it was too late.', ' Redbull never actually gave him wings.',
            ' socks are just shoes for the house.', ' he could save big on his car insurance by switching Geico.',
            ' racecar spelled backwards is racecar.', ' he forgot to feed his dog.']

#***CHANGING THIS***

# Below is the output. mytext will begin to choose arguments from the variables.
mytext = (random.choice(when) +
          'an ' +
          random.choice(who) +
          ' named ' +
          random.choice(name) +
          ' went to the ' +
          random.choice(went) +
          ' to find ' +
          random.choice(why) +
          'but instead, found a ' +
          random.choice(happened) +
          ' Suddenly' +
          random.choice(speechless) +
          ' appeared, holding a' +
          random.choice(appeared) +
          ' Then, he' +
          random.choice(then) +
          ' "I have a quest for you, young adventurer.", he explained. ' +
          '"I need you to bring me a' +
          random.choice(need) +
          ' The adventurer obliged, vowing to accomplish the task. ' +
          'A few days later, the adventurer realized' +
          random.choice(realized) +
          ' Although he vowed to accomplish the task he had been given, he realized that this was far too important to ignore, and traveled back home.')

# This will define the language. Other languages may be used as well, as long as they are supported by gTTS
language = 'en'

# This will determine the audio output.
output = gTTS(text=mytext, lang=language, slow=False)

# This will save the file into an mp3 format called output.mp3
output.save("output.mp3")

# This will start output.mp3
os.system("start output.mp3")

# This will exit the script automatically.
raise SystemExit
