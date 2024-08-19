from PIL import Image, ImageDraw, ImageFont
import matplotlib.pyplot as plt

# Load your Rakshabandhan image
background_image_path = 'rakshabandhan_image.jpg'  # Replace with your image path
background_image = Image.open(background_image_path)

# Prepare text
text = "Happy Rakshabandhan to you, Vaishnavi Didi"

# Set up font and size
try:
    font = ImageFont.truetype("arial.ttf", 40)  # Change the font and size as needed
except IOError:
    font = ImageFont.load_default()

# Create an ImageDraw object
draw = ImageDraw.Draw(background_image)

# Define text position
text_position = (50, 50)  # Change position as needed

# Define text color
text_color = (255, 255, 255)  # White text

# Add text to the image
draw.text(text_position, text, font=font, fill=text_color)

# Show the image with the added text
plt.imshow(background_image)
plt.axis('off')  # Hide axes
plt.show()
