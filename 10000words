import random

# Function to duplicate text
def duplicate_text(text, n):
    return text * n

# Function to save the duplicate result to a file
def save_result(result, file_name):
    with open(file_name, "w") as f:
        f.write(result)

# Function to create a random duplicate
def random_duplicate(text, n):
    result = ""
    for i in range(n):
        result += text[random.randint(0, len(text) - 1)]
    return result

# Main program
print("Welcome to the Python program that can replicate and duplicate a word or phrase.")

# Create a variable to store the program status
running = True

# Create a loop to receive user input and provide a response
while running:
    # Request input from the user
    user_input = input("Enter the word or phrase you want to duplicate: ")

    # Check if the user input is valid
    if user_input.isalnum() or user_input.isspace() or user_input.isprintable():
        # Request the number of duplicates from the user
        n = int(input("Enter the number of duplicates (maximum 20000): "))

        # Check if the number of duplicates is valid
        if n > 0 and n <= 20000:
            # Display the option to save the duplicate result to a file
            save = input("Save the duplicate result to a file? (y/n): ")

            if save == "y":
                file_name = input("Enter the file name to save the result: ")
                result = duplicate_text(user_input, n)
                save_result(result, file_name)
                print("Duplicate result successfully saved to file.")
            else:
                result = duplicate_text(user_input, n)
                print(f"Duplicate result: {result}")
        else:
            print("Sorry, the number of duplicates must be between 1 and 20000.")
    elif user_input == "keluar":
        # Change the program status to False to stop the loop
        running = False
        # Give a farewell response to the user
        print("Thank you for using this program.")
    else:
        # Give a response that the user input is not valid
        print("Sorry, your input must be letters, numbers, spaces, or printable symbols.")
