# Michael
#youtube auto-viewer
import webbrowser
import time
import os

# Ask the user for the link
link = input("Please input your web address: ")

# Ask the user for prefered number of tabs
number = int(input("How many views? "))

# Ask the user for prefered number of minutes
minutes = float(input("How many minutes? "))

# Initialize the counter
count = 0

# Loop until the number of views have been reached
while count < number:
    # Open the link in the web browser
    webbrowser.open(link)
    # Run the program for the number of minutes prefered 
    time.sleep(60 * minutes)
    # Kill the app
    os.system("taskkill /im chrome.exe /f")
    # Increase the count
    count = count + 1
