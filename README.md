# Password_Generator
Cyber Security Password

import random
import string   

def generate_password(length=12):
    #Define characters to be used in password:
    characters = string.ascii_letters + string.ascii_letters + string.punctuation

    #Generate a password by Randomly selecting characters
    password = ''.join(random.choice(characters) for _ in range (length))

    return password

if __name__ == "__main__":
    password_length = int(input("Enter the length of the password: "))

    if password_length < 5:
        print ("Password length must be atleast more than 5 characters")
    else:
        generated_password = generate_password(password_length)
        print ("Generated password: ", generated_password)
