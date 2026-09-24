# Project-Rock-Paper.Scissors-CSE1021
This is a project of my Python Program of a Game, that i built recently in accordance to my SEM1

    import random

    print("!!!!!ROCK PAPER SCISSORS!!!!")

    choices = ["rock", "paper", "scissors"]

    playerscore = 0
    compscore = 0


    while True:
        print("\nChoose one:")
        print("1. rock")
        print("2. paper")
        print("3. scissors")
        print("4. end")
    
        choice = input("Your choice: ")

        if choice == "4":
            break
        if choice not in ["1", "2", "3"]:
            print("Invalid choice! Try again.")
            continue

        x = choices[int(choice) - 1]                #PLAYER'S CHOICE
        y = random.choice(choices)                  #COMPUTER'S CHOICE

        print("\nYou chose:", x)
        print("Computer chose:", y)

        if y == x:
            print("DRAW.")

        elif ((x == "rock" and y == "scissors")
            or
            (x == "paper" and y == "rock")
            or
            (x == "scissors" and y == "paper")):
            print("WON.")
            playerscore += 1

        else:
            print("LOSE.")
            compscore += 1

        print("Your Score:", playerscore)
        print("Computer Score:", compscore)

    print("GAME OVER.")

    print("Final score:", "YOU",  playerscore, "-" ,"COMPUTER"  compscore)

    print("Thanks! Come Again.")
