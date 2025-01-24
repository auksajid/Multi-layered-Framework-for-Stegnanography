# Multi-layered-Framework-for-Stegnanography
Efficient framework that integrates cryptography and steganography techniques
The code is written in Python and it appears to be performing the following tasks:

Encryption and Decryption using AES:

It defines functions to generate a random AES key, encrypt text using AES in Electronic Codebook Mode (ECB), and decrypt ciphertext back to the original text.
The encryption process pads the text to ensure it's a multiple of 16 bytes before encryption with AES.
Image Steganography:

It defines functions to embed the encrypted text (ciphertext) into an image using Least Significant Bit (LSB) steganography and extract the ciphertext back from the image.
During embedding, for each channel of each pixel in the image, the LSB (Least Significant Bit) is replaced with the corresponding bit from the ciphertext.
Extraction retrieves the hidden bits from the image and combines them to form the original ciphertext.
3D Image Visualization (Example):

It includes functions to generate example 3D points (commented out) and visualize a 3D model from an image.
The image_to_3d function takes an image path as input, extracts the pixel values and uses them to create a 3D surface plot using matplotlib.
mportant Notes:

This code implements a simple example of LSB steganography, which is easily detectable. In practice, more sophisticated steganography techniques are used.
AES in ECB mode is not recommended for secure encryption due to vulnerabilities. Consider using a more secure mode like CBC or GCM.
This code snippet utilizes libraries like cv2, numpy, Crypto.Cipher, PIL, and matplotlib. You might need to install these libraries before running the code.
