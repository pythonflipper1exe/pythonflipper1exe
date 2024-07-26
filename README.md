
#Code is here now!
#A very basic python coded bot for absolute begginers

#READ THE ATTACHED DOCUMENT FOR SEEING THE COMMANDS THAT BOT SUPPORTS! THIS PROJECT IS NOT TESTED BY ME (coder). TEST IT AND AND TELL IF ANY PROBLEMS IN THE CODE!

import random

#Bot Responses List

bot_greet = ['Howdy!', 'Nice to meet you!', 'Hello Human!']
bot_bye = ['Bye!', 'Come back soon!', "I'll miss you!"]
fallback = ["Didn't understand what you said..."]

#Human (user) Response List

user_greet = ['Hi', 'hi', 'hello', 'Hello', 'Howdy', 'how are you'] # if the user does not input these words then it prints fallback
user_bye = ['bye', 'Bye', 'cya', 'see you']

#mystery message

msg = ['You are looking beautiful today!', 'What a charm!', 'Pong!', 'Ping!']

#main code

print("Bot: I'll be your chatbot for today! Say a nice 'hi' to start!")
user = input("You:  ").strip()
if user in user_greet:
    print(random.choice(bot_greet))#prints any a random message from bot_greet list
    user_inp = input("Bot: write '!surprise' to recieve a mystery message! Say be bye to end the chat... ").strip()
if user_inp == '!surprise':
    print(random.choice(msg))
elif user_inp in user_bye:
    print(random.choice(bot_bye))
elif user_inp in user_greet:
    print(random.choice(bot_greet))
else:
    print(fallback)
ask = input("Want to play a quiz (y/n):  ").strip()
if ask == 'y':
    ques_1 = input("Capital of India (only enter in lower case): ").strip()
    if ques_1 == 'delhi' or 'new delhi':
        print("Bot: Correct!")
    ques_2 = input("which language has the extension '.py' (only enter in lower case):  ").strip()
    if ques_2 == 'python':
        print("Bot: Correct!")
        print("QUIZ ENDED...")
elif ask == 'n':
    print("Ok...")
else:
    print(fallback)
print("Bot: Say 'hi' or 'bye' or '!surprise' to recieve a message!")
enter = input("You: ").strip()
#END
