# python
import tkinter as tk
import random

# Function to draw a colorful pattern
def draw_pattern():
    colors = ['red', 'green', 'blue', 'orange', 'purple', 'yellow']
    canvas.delete("all")  # Clear the canvas

    for _ in range(100):
        x1 = random.randint(0, 300)
        y1 = random.randint(0, 300)
        x2 = x1 + random.randint(20, 100)
        y2 = y1 + random.randint(20, 100)

        color = random.choice(colors)
        canvas.create_rectangle(x1, y1, x2, y2, fill=color)

# Create the main window
root = tk.Tk()
root.title("Cool Pattern Generator")

# Create a canvas to draw the pattern
canvas = tk.Canvas(root, width=300, height=300)
canvas.pack()

# Create a button to generate the pattern
button = tk.Button(root, text="Generate Pattern", command=draw_pattern)
button.pack()

# Run the GUI application
root.mainloop()

