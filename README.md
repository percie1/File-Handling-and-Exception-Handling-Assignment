# File-Handling-and-Exception-Handling-Assignment

# Read from input.txt and write modified content to output.txt


    with open("input.txt", "r") as infile:
        content = infile.read()

    # Modify content (e.g., convert to uppercase)
    modified_content = content.upper()

    with open("output.txt", "w") as outfile:
        outfile.write(modified_content)

    print("Modified content written to output.txt")




# Ask the user for a filename and handle errors


    with open(filename, "r") as file:
        print("\nFile contents:\n")
        print(file.read())

except FileNotFoundError:
    print(f"Error: The file '{filename}' does not exist.")
except PermissionError:
    print(f"Error: You do not have permission to read '{filename}'.")
except Exception as e:
    print("An unexpected error occurred:", e)

