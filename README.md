# simple-registration-form
import tkinter as tk
class RegistrationForm:
def __init__(self, master):
self.master = master
master.title("Registration Form")
#Labels
self.name_label = tk.Label(master, text="Name:")
self.name_label.grid(row=0, column=0)
self.name_entry = tk.Entry(master)
self.name_entry.grid(row=0, column=1)
self.email_label = tk.Label(master, text="Email:")
self.email_label.grid(row=1, column=0)
self.email_entry = tk.Entry(master)
self.email_entry.grid(row=1, column=1)
self.password_label = tk.Label(master, text="Password:")
self.password_label.grid(row=2, column=0)
self.password_entry = tk.Entry(master, show="*")
self.password_entry.grid(row=2, column=1)
self.confirm_password_label = tk.Label(master, text="Confirm Password:")
self.confirm_password_label.grid(row=3, column=0)
self.confirm_password_entry = tk.Entry(master, show="*")
self.confirm_password_entry.grid(row=3, column=1)
# Create submit button
self.submit_button = tk.Button(master, text="Register", command=self.submit_form)
self.submit_button.grid(row=4, column=1)

def submit_form(self):
# Get the values from the entry fields
name = self.name_entry.get()
email = self.email_entry.get()
password = self.password_entry.get()
confirm_password = self.confirm_password_entry.get()

# Check if the passwords match
if password != confirm_password:
print("Passwords do not match")
return

# Print the registration details
print("Registration successful!")
print("Name:", name)
print("Email:", email)
print("Password:", password)

root = tk.Tk()
my_form = RegistrationForm(root)
root.mainloop()
