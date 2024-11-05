# biglietto.net


https://colab.research.google.com/drive/1ZmCERzLCymrV2ijvaVnOpPkUMyPFVsCw
from google.colab import files
import base64

# Carica la foto
uploaded = files.upload()

# Codifica in Base64
for filename in uploaded.keys():
    with open(filename, "rb") as image_file:
        base64_string = base64.b64encode(image_file.read()).decode('utf-8')
        print("Codice Base64 dell'immagine:")
        print(base64_string)
