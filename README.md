import tkinter as tk
from tkinter import font

# Function to display the name and dream in a fancy way
def display_fancy_info():
    name = entry_name.get()
    dream = entry_dream.get()

    # Create custom font
    custom_font = font.Font(family="Arial", size=14, weight="bold", underline=1)

    # Display the name and dream with custom font
    label_result.config(text=f"Name: {name}\nDream: {dream}", font=custom_font)

# Create the main window
root = tk.Tk()
root.title("Fancy Dream Display")

# Create a frame for input
input_frame = tk.Frame(root)
input_frame.pack(pady=10)

# Create labels and entry widgets for name and dream
label_name = tk.Label(input_frame, text="Enter your name:")
label_name.grid(row=0, column=0, padx=5, pady=5)
entry_name = tk.Entry(input_frame)
entry_name.grid(row=0, column=1, padx=5, pady=5)

label_dream = tk.Label(input_frame, text="Enter your dream:")
label_dream.grid(row=1, column=0, padx=5, pady=5)
entry_dream = tk.Entry(input_frame)
entry_dream.grid(row=1, column=1, padx=5, pady=5)

# Create a button to display the fancy info
display_button = tk.Button(root, text="Display Fancy Info", command=display_fancy_info)
display_button.pack(pady=10)

# Create a label to display the result
label_result = tk.Label(root, text="")
label_result.pack()

root.mainloop()


