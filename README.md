"""
projekt_2.py: Druhý projekt do Engeto Online Python Akademie

author = Petr Kulig
email: petrkg@centrum.cz
discord: Petr Kulig#4490
"""

print("Hi there")
print("_" * 40)
print("I've generated a random 4 digit number for you.\n Let's play a bulls and cows game.")
print("_" * 40)
print("enter with the number below.\n" + " " * 40)
while True:
    import random

    digits = list(range(1000, 9999))
    digits2 = str(random.choice(digits))

    print("Computer just created secure digits")


    player = input("Please, put your 4 digits number here")

    #if player < 1000 or player > 9999:
    if len(player) != 4:
        print("You have to write 4  digits")

        print(input("Please, put your 4 digits number here"))


    elif player.startswith("0"):
        print(input("Please, put your 4 digits number here again, without 0"))


    else:
        print("You put this number", player)
        break





while True:

    match = 0
    cows = 0
    for i, v in enumerate(str(player)):
        if v == str(digits2)[i]:
            match = match +1
            print(f" You have {match}bulls")


            #print(f"You  get{match} bull")
        elif v in str(digits2):
            cows = cows + 1


        print(f"You get {match} bulls and { cows }cows")
    break

    if match == 4:
        print(" You win")
    if match < 4:
        print("try again")
        continue
