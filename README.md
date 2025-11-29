# password-strength-checker
A simple Python tool that checks the strength of a password based on length and character complexity.
Password Strength Checker (Python)

This is a simple Python security tool that checks how strong a password is using basic rules:
Length
Uppercase letters
Lowercase letters
Numbers
Special characters

 Features
Tells you if a password is Weak, Medium, or Strong
Shows which requirements are missing
Beginner-friendly Python tool
Code (password_checker.py)

Create a file named password_checker.py and paste this code:
import re
def check_password_strength(password):
    score = 0
    if len(password) >= 8:
        score += 1
    if re.search(r"[A-Z]", password):
        score += 1
    if re.search(r"[a-z]", password):
        score += 1
    if re.search(r"[0-9]", password):
        score += 1
    if re.search(r"[!@#$%^&*(),.?\":{}|<>]", password):
        score += 1
    if score <= 2:
        return "Weak Password"
    elif score == 3 or score == 4:
        return "Medium Strength"
    else:
        return "Strong Password"
password = input("Enter a password: ")
print(check_password_strength(password))

 How to Run
python3 password_checker.py

 Summary
This tool is part of my cybersecurity learning journey.
More Python security tools coming soon.
