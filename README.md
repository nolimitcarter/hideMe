# Steganography project that was made with Python and a random .png file.
### A Python program that hides and retrieves text from .png file pictures.  

Requirements: 
pip
image, pip install image

Usage: 
python hide.py
python hide.py -e picture.png(whatever picture you have in the repo) to add the encrypted message
python hide.py -d picture.png to decrypt the message contained in the photo


Several functions are used for manipulating the data: rgb2hex, hex2rgb, str2bin, bin2str


How it works: 
It will open the image and look at the pixels in hexadecimal. If the pixels blue channel falls in the 0-5 range then 1 bit of information will be stored. It ends the stream with a delimiter of fifteen 1's and a 0 to take up two bytes. When it is time to retrieve, it pulls all the blue bits of 0 and 1 until the stream obtains the delimiter of fifteen 1's and a 0.  
