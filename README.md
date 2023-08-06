Encrypt_AES which provide methods to encrypt and decrypt strings and images using AES encryption algorithm CBC mode.

Import the necessary Libraires:

    * pip install pycryptodome
    * pip install pillow
    
Imports the following Modules:

    * Crypto.Cipher.AES : Module provide the implemention of the AES algorithm
    * Crypto.Util.Padding : Module provide functions for adding and removing padding from data to be encrypted
    * os : Module provide a way to generate a random initialization vector(iv) to use in the encryption process
    * PIL.Image : Module provide the ability to read and write image file

The Encrypt_AES class has several methods:

    * __init__ : Initializes the class instance with a key.

    * encrypt_string(self, plaintext_str): Encrypts a plaintext string using the AES algorithm in CBC mode, and returns the IV and the ciphertext bytes.
    
    * decrypt_string(self, ciphertext): Decrypts the given ciphertext bytes using the AES algorithm in CBC mode, and returns the plaintext string.
    
    * encrypt_image(self, image_path): Reads an image from the given image_path, encrypts it using the AES algorithm in CBC mode, and returns the IV and the ciphertext bytes.
    
    * decrypt_image(self, ciphertext, output_path): Decrypts the given image ciphertext bytes using the AES algorithm in CBC mode, and writes the resulting image to the file at output_path.
    
    * encrypt_strings(self, plaintext_strings): Encrypts multiple plaintext strings and returns a list of their ciphertexts.
    
    * decrypt_strings(self, ciphertexts): Decrypts a list of ciphertexts and returns a list of their plaintext strings.
    
    * encrypt_images(self, image_paths): Encrypts multiple images and returns a list of their ciphertexts.
    
    * decrypt_images(self, ciphertexts, output_dir): Decrypts a list of image ciphertexts and writes the resulting images to the files in the given output_dir.
    
    
Ecrypt_AES class is created using a randomly generated 32-byte key.Then used to encrypt and decrypt multiple strings and images.The original plaintext strings and image file paths are provided and the encrypted ciphertexts are printed. 
After decryption the resulting plaintext strings and decrypted images are printed to confirm that encryption and decryption works correctly.
