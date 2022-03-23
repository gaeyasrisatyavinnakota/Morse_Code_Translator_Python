# Morse Code Translator Python
The code shown below is used to implement the Morse Code Translator in Python
```
"""
This code takes in the user input (only alphabetical text or morse code )
and translates it either to a piece of text if the input from user is a piece of morse code
or translates it to a piece of morse code if the input from user is a piece of text
"""

# Morse Translator

def main():
    print("This code translates a piece of text into morse code and piece of morse code into text")
    user_input = input("Enter the piece of text or morse code you want to translate : ")
    print(morse(user_input))
    choice = input("Do you want to translate another piece of text or morse code? if YES enter 1 if NO enter 0 : ")
    while True:
        if choice == '1':
            user_input = input("Enter the piece of text or morse code you want to translate : ")
            print(morse(user_input))
            choice = input("Do you want to translate another piece of text or morse code? if YES enter 1 if NO enter 0 : ")
        elif choice == '0':
            print("Thank you for using the translator")
            break
        else:
            print("Please enter a valid choice")
            choice = input("Do you want to translate another piece of text or morse code? if YES enter 1 if NO enter 0 : ")


#--------This function does the main part of translation--------#
def morse(user_input):
    encrypt = {'A':'.-', 'B':'-...', 'C':'-.-.',
               'D':'-..', 'E':'.', 'F':'..-.',
               'G':'--.', 'H':'....', 'I':'..',
               'J':'.---', 'K':'-.-', 'L':'.-..',
               'M':'--', 'N':'-.', 'O':'---',
               'P':'.--.', 'Q':'--.-', 'R':'.-.',
               'S':'...', 'T':'-', 'U':'..-',
               'V':'...-', 'W':'.--', 'X':'-..-',
               'Y':'-.--', 'Z':'--..', ' ':'.....'}
    decrypt = {v: k for k, v in encrypt.items()}
   
    if '-' in user_input:
        return ''.join(decrypt[i] for i in user_input.split())
    return ' '.join(encrypt[i] for i in user_input.upper())


if __name__ == "__main__":
    main()
```
