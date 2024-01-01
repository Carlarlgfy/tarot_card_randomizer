import tkinter as tk
from PIL import Image, ImageTk
from random import sample
import os

# List of your tarot card image file names
card_images = ['Pents06.jpg', 'Pents12.jpg', 'Pents13.jpg', 'Pents07.jpg', 'Pents11.jpg', 'Pents05.jpg', 'Pents04.jpg', 'Pents10.jpg', 'Pents14.jpg', 'Pents01.jpg', 'Wands08.jpg', 'Swords08.jpg', 'Cups09.jpg', 'Pents03.jpg', 'Pents02.jpg', 'Cups08.jpg', 'Swords09.jpg', 'Wands10.jpg', 'Wands04.jpg', 'Swords04.jpg', 'Swords10.jpg', 'Cups05.jpg', 'Cups11.jpg', 'Cups10.jpg', 'Cups04.jpg', 'Swords11.jpg', 'Swords05.jpg', 'Wands05.jpg', 'Wands11.jpg', 'Wands07.jpg', 'Wands13.jpg', 'Swords13.jpg', 'Swords07.jpg', 'Cups12.jpg', 'Cups06.jpg', 'Cups07.jpg', 'Cups13.jpg', 'Swords06.jpg', 'Swords12.jpg', 'Wands12.jpg', 'Wands06.jpg', 'Tarot_Nine_of_Wands.jpg', 'Wands02.jpg', 'Swords02.jpg', 'Cups03.jpg', 'Pents09.jpg', 'Pents08.jpg', 'Cups02.jpg', 'Swords03.jpg', 'Wands03.jpg', 'Wands01.jpg', 'Swords01.jpg', 'Cups14.jpg', 'Cups01.jpg', 'Swords14.jpg', 'Wands14.jpg', 'the_hermit.png']  # Your list of images

# Path to the tarot card images folder
image_folder = 'tarot_cards_2'

# Initialize the main window
root = tk.Tk()
root.title("Tarot Card Randomizer")

# Set the initial size of the window
root.geometry("1200x800")  # Width x Height

# Function to draw three random cards
def draw_cards():
    # Clear previous cards
    for widget in frame.winfo_children():
        widget.destroy()

    # Select three random card images
    selected_cards = sample(card_images, 3)

    # Display the cards
    for card_image in selected_cards:
        image_path = os.path.join(image_folder, card_image)
        img = Image.open(image_path)

        # Resize the images to a larger size
        img = img.resize((350, 525))  # Adjust the size as needed

        img = ImageTk.PhotoImage(img)
        label = tk.Label(frame, image=img)
        label.image = img  # Keep a reference
        label.pack(side=tk.LEFT, padx=10)

# Create a frame to hold the card images
frame = tk.Frame(root)
frame.pack(pady=20)

# Add buttons
draw_button = tk.Button(root, text="Draw Cards", command=draw_cards)
draw_button.pack(side=tk.LEFT, padx=20)

quit_button = tk.Button(root, text="Quit", command=root.destroy)
quit_button.pack(side=tk.RIGHT, padx=20)

root.mainloop()
