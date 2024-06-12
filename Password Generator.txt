import random
import string

def generate_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for i in range(length))
    return password

def main():
    length = int(input("Enter the length of the password you want to generate: "))
    if length < 1:
        print("Invalid length! Password length must be at least 1.")
    else:
        password = generate_password(length)
        print("Generated Password:", password)

if __name__ == "__main__":
    main()
