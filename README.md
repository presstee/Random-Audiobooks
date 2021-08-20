#!/usr/bin/env python3

# Allows for interaction with my operating system
import os
# This will import from Google Text-To-Speech. which will allow text output to be converted into an audio file.
from gtts import gTTS
# This will give the output a random argument
import random

# Title: The (Almost) Adventures of Timmy.

# Once upon a time, a boy named Timmy, went to the
went = ['skate park', 'carnival', 'mall', 'pond', 'art gallery', 'zoo', 'gym', 'bank', 'hospital', 'Nickelback concert',
        'block party', 'football game', 'mountain', 'beach', 'candy shop', 'library', 'movie theater', 'Disney World']
# because he was looking for
why = ['a job,', 'friends,', 'a can of soda,', 'a tutor, ', 'a mentor,', 'breakfast,', 'advice,', 'food,',
       'quality alone time,', 'a musical instrument,', 'a stick of butter,', 'a mentor,', 'a pair of shoes,']
# but instead, Timmy found a
happened = ['wallet.', 'spoon.', 'shoe.', 'strange cave.', 'cat.', 'leopard.', 'panda.', 'bumper sticker.', 'honda.',
            'weird looking mouse.', 'mirror.', 'shoe.', 'cave.', 'cat.', 'sock.', 'chicken coop.', 'pencil.']
# Suddenly,
speechless = ['kermit The Frog', 'Harry Potter', 'Homer Simpson', 'Gordon Ramsey', 'Captain America',
              'Dwayne Johnson', 'Rick Sanchez', 'Elon Musk', 'A little old man', 'Peter Griffin', 'Florida Man']
# appeared, holding what seemed to be a
appeared = ['frying pan.', 'cookie.', 'bottle of gatorade.', 'plastic bag.', 'baby.', 'Mtn Dew.', 'fork!',
            'letter.', 'pool stick!.', 'book.', 'head of lettuce.', 'carrot.', 'bowtie.', 'brownie.', 'basket.',
            'chalupa.', 'microphone.', 'Big Mac.', 'Nintendo Switch.']
# Then, Timmy
then = ['started panicking.', 'remained calm.', 'started singing.', 'gracefully slipped on a banana.',
        'started rapping for no apparent reason.', 'started to cry.', 'started walking back slowly.',
        'started to look puzzled...']
# "Hello Timmy", he said.
# Timmy Replied, "What do you want from me? And how do you know my name?"
# "I have no time to explain" he said. "I have a quest for you Timmy. I need you to bring me a
need = ['garden hose."', 'pickle jar."', 'soda."', 't-shirt."', 'bottle of water."', 'waffle."', 'pizza."',
        'Redbull."', ' clock."', ' bag of chips."', 'bowl of cereal."', 'helicopter."', 'million dollars."',
        'sandwich."', 'helicopter."', 'pencil sharpener."', 'pair of socks."', 'letter opener."']
# Timmy, seeming fairly puzzled, replied "Where on Earth do I find that?."
# Timmy got no reply..
# "Well okay, I guess I will get to it.", Timmy said to himself.
# As Timmy was walking away, he stopped.. Timmy realized
abandoned = ['he was hungry.', 'his extended warranty was almost expired.', 'he missed a call from his mother.',
             'it was all a game.', 'it was passed his bedtime.','he had been bamboozled.', 'he was too tired to help.',
             'socks are just shoes for the house.', 'he could save big on his car by insurance by switching Geico.'
             'that Redbull he drank earlier never actually gave him wings.']
# Coming to this realization, Timmy turned back around, and reluctantly turned down the quest... The end.

# Below is the formula
mytext = ('Once upon a time, a boy named Timmy, went to the ' +
          random.choice(went) +
          ' because he was looking for ' +
          random.choice(why) +
          ' but instead, Timmy found a ' +
          random.choice(happened) +
          ' Suddenly, ' +
          random.choice(speechless) +
          ' appeared, holding what seemed to be a ' +
          random.choice(appeared) +
          ' Then, Timmy ' +
          random.choice(then) +
          ' "Hello Timmy" he said. ' +
          ' Timmy replied, "What do you want from me? And how do you know my name?" ' +
          ' "I have no time to explain" he said. "I have a quest for you Timmy. I need you to bring me a ' +
          random.choice(need) +
          ' Timmy, seeming fairly puzzled, replied "Where on Earth do I find that?" ' +
          ' Timmy got no reply. ' +
          ' "Well okay, I guess I will get to it.", Timmy said to himself. ' +
          ' As Timmy was walking away, he stopped.. Timmy realized ' +
          random.choice(abandoned) +
          ' Coming to this realization, Timmy turned back around, and reluctantly turned down the quest... The end. ')

# This will define the language. Other languages may be used as well, as long as they are supported by gTTS
language = 'en'

# This will determine the audio output.
output = gTTS(text=mytext, lang=language, slow=False)

# This will save the file into an mp3 format called output.mp3
output.save("output.mp3")

# This will start output.mp3
os.system("start output.mp3")

# This will exit the script.
quit()
