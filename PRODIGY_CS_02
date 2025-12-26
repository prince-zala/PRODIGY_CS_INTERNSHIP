from PIL import Image
import os

def encrypt_decrypt_image(input_image_path, output_image_path, key):
    if not os.path.exists(input_image_path):
        print(" Input image not found.")
        return

    image = Image.open(input_image_path).convert("RGB")  # FIX HERE
    pixels = image.load()

    width, height = image.size

    for x in range(width):
        for y in range(height):
            r, g, b = pixels[x, y]
            pixels[x, y] = (r ^ key, g ^ key, b ^ key)

    image.save(output_image_path)
    print("✅ Operation completed successfully!")

# -------- Main Program --------
print("Image Encryption Tool")
print("1. Encrypt Image")
print("2. Decrypt Image")

choice = input("Enter choice (1/2): ")

input_image = input("Enter input image path: ")
output_image = input("Enter output image path: ")
key = int(input("Enter encryption key (0-255): "))

if choice == "1":
    encrypt_decrypt_image(input_image, output_image, key)
    print("Image Encrypted Successfully!")

elif choice == "2":
    encrypt_decrypt_image(input_image, output_image, key)
    print("Image Decrypted Successfully!")

else:
    print("Invalid choice!")
