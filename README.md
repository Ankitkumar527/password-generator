# password-generator
import random
import string

def generate_password(length):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def generate_passwords(length, count):
    return [generate_password(length) for _ in range(count)]

if __name__ == "__main__":
    # Get user input for password length and number of passwords
    length = int(input("Enter the desired password length: "))
    count = int(input("Enter the number of passwords to generate: "))

    # Generate passwords
    passwords = generate_passwords(length, count)

    # Print the generated passwords
    for idx, password in enumerate(passwords, start=1):
        print(f"Password {idx}: {password}")
