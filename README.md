# -Python-Project-11
#11 Sum the first two digits of an number

def main() -> None:
    def inputnumber() -> str:
        while True:
            inputnumber = input("Type a two digit number: ")
            if not inputnumber.isdigit():
                print("No,no,no! Put a valid number!\n")
            elif len(inputnumber) < 2:
                print("Hey! That\'s too short! Please, type a two digit number.\n")
            elif len(inputnumber) > 2:
                print("Hey! That\'s too long! Please, type a two digit number.\n")
            else:
                return inputnumber

    def yes_no(message: str) -> bool:
        while True:
            userinput = input(message).lower()
            if userinput == "yes":
                return True
            elif userinput == "no":
                return False
            else:
                print("Please, use 'yes' or 'no'.")

    while True:
        number = inputnumber()
        total = int(number[0]) + int(number[1])
        print(f"{total}\n")

        if yes_no("Do you want to try again?\n"):
            print("Okay! Don\'t forget the rules!\n")
        else:
            print("Good bye!")
            return


main()
