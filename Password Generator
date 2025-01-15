import random
import string
import tkinter as tk
from tkinter import messagebox

def generate_password(length=12):
    all_characters = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(all_characters) for _ in range(length))

def show_password():
    try:
        length = int(password_length_entry.get())
        if length < 4:
            messagebox.showwarning("Invalid Length", "Password length should be at least 4.")
            return
        password = generate_password(length)
        password_display.delete(0, tk.END)
        password_display.insert(0, password)
    except ValueError:
        messagebox.showerror("Input Error", "Please enter a valid number.")

root = tk.Tk()
root.title("Password Generator")
root.geometry("400x300")

length_label = tk.Label(root, text="Enter password length:")
length_label.pack(pady=10)

password_length_entry = tk.Entry(root)
password_length_entry.insert(0, "12")
password_length_entry.pack(pady=10)

generate_button = tk.Button(root, text="Generate Password", command=show_password)
generate_button.pack(pady=10)

password_display = tk.Entry(root, width=40)
password_display.pack(pady=10)

root.mainloop()
