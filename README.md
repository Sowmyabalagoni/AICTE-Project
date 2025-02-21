# AICTE-Project

# Image Steganography

This project implements a simple image steganography technique where a secret message can be encoded into an image and later decoded using a passcode. The message is hidden in the least significant bits (LSBs) of the image's pixel values, making the changes visually undetectable.

## Features

- **Encoding**: Hide a secret message inside an image.
- **Decoding**: Extract the hidden message from the image.
- **Passcode Protection**: Only authorized users with the correct passcode can decrypt the message.

## Requirements

- Python 3.x
- OpenCV (for image manipulation)
  
You can install the required packages by running:

```bash
pip install opencv-python
```

## Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/image-steganography.git
   cd image-steganography
   ```

2. **Run the script**:
   ```bash
   python steganography.py
   ```

3. **Steps for Encoding**:
   - You will be prompted to enter the secret message you want to hide in the image.
   - Enter a passcode for encryption (used later for decryption).
   - The script will modify the image to encode the secret message in the least significant bits of the image pixels.
   - The modified image will be saved as `encryptedImage.jpg`.

4. **Steps for Decoding**:
   - After you encode a message, you can decrypt it by running the script again.
   - You will be prompted to enter the passcode used during encoding.
   - If the correct passcode is entered, the hidden message will be decrypted and displayed on the screen.
   
## How it Works

1. **Encoding**: 
   - The secret message is converted to a binary string. Each bit of the message is hidden in the least significant bit (LSB) of the image's pixel values.
   - The image is modified by replacing the LSBs of the pixel color channels (RGB) with the bits of the message.

2. **Decoding**:
   - The image is scanned, and the LSB of each pixel color channel is extracted to reconstruct the binary message.
   - The binary string is then converted back to text.

3. **Passcode Protection**:
   - A passcode is required for decrypting the message. This ensures that only authorized users can access the hidden message.

## Example

### Encoding Example:
```
Enter secret message: Hello World
Enter a passcode: mySecret123
```

After encoding, the image will be saved as `encryptedImage.jpg`. You can view this image as you normally would.

### Decoding Example:
```
Enter passcode for Decryption: mySecret123
Decrypted message: Hello World
```

If the passcode is incorrect, the message will not be decrypted.

## Notes

- Ensure that the image you use has enough pixels to hold the entire message. The message's length will determine how many pixels need to be modified.
- The script works with `.jpg` images, but you can adapt it to other image formats by changing the file extension accordingly.
- The encoding process works by modifying the least significant bit (LSB) of each pixel’s color channel, ensuring that the visual change to the image is minimal.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### To use the above in your GitHub repository:

1. Create a file named `README.md` in the root directory of your repository.
2. Copy and paste the content above into that file.
3. Commit the file to your repository with:

```bash
git add README.md
git commit -m "Add README for steganography project"
git push origin main
```

This will provide a clean and informative README for anyone browsing your repository on GitHub.
