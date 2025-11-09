# Files-Exceptions-and-Errors-in-Python
# task 1
try:
    with open("sample.txt", "r") as f:
        print("File exists: and reading file content\n")
        for line in f:
            print(line.strip())

except FileNotFoundError:
    print("File does not exist")

# task 2
user_input = input("Enter some text to write to the file: ")

with open("output.txt", "w") as file:
    file.write(user_input + "\n")  # Write user input and add a newline

print("Data written to file successfully.")

additional_input = input("Enter additional text to append to the file: ")

with open("output.txt", "a") as file:
    file.write(additional_input + "\n")  # Append additional data

print("Data appended to file successfully.")

print("\nFinal content of the file:")
with open("output.txt", "r") as file:
    content = file.read()
    print(content)
