print("Caesar Cipher Encryption (No Functions)")

text = input("Enter the message to encrypt: ")
k = int(input("Enter the shift value (1-25): "))

if not 1 <= k <= 25:
    print("Shift value must be between 1 and 25.")
else:
    encrypted_text = ""
    for char in text:
        if char.isalpha():
            shift_base = ord('A') if char.isupper() else ord('a')
            shifted = (ord(char) - shift_base + k) % 26 + shift_base
            encrypted_text += chr(shifted)
        else:
            encrypted_text += char

    print("Encrypted message:", encrypted_text)
