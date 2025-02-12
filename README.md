This project extracts text from an image using **Tesseract OCR**, converts it to speech using **gTTS (Google Text-to-Speech)**, and plays the generated audio in Google Colab.  

## 📌 Requirements  
Before running the script, install the necessary dependencies:  
```bash
!sudo apt install tesseract-ocr -y
!pip install pytesseract gTTS Pillow]

🚀 How to Run
# Import necessary libraries
import pytesseract
from PIL import Image
import gtts
from IPython.display import Audio

# Load the image
img = Image.open('/content/Picture1.png')  # Replace with your image file

# Extract text from the image
result = pytesseract.image_to_string(img)
print("Extracted Text:\n", result)

# Convert text to speech
tts = gtts.gTTS(result)
tts.save("hello.mp3")

# Play the generated audio in Colab
Audio("hello.mp3", autoplay=True)
```
🎯 Expected Output

    Extracted Text from the image will be displayed.
    Generated Speech will be played directly inside Colab.
