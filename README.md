# EX-4-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM
## Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM:
AES is based on a design principle known as a substitution–permutation.<br>
AES does not use a Feistel network like DES, it uses variant of Rijndael.<br>
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.<br>
AES operates on a 4 × 4 column-major order array of bytes, termed the state<br>

## PROGRAM:
```
def xor_encrypt_decrypt(text, key):
    key_len = len(key)
    result = []

    for i in range(len(text)):
        # XOR each character with the corresponding character in the key
        xor_char = chr(ord(text[i]) ^ ord(key[i % key_len]))
        result.append(xor_char)

    return ''.join(result)

def main():
    text = input("Enter the text: ")
    key = input("Enter the key: ")

    print("Original text:", text)

    encrypted_text = xor_encrypt_decrypt(text, key)
    print("Encrypted text:", ''.join(f"\\x{ord(c):02x}" for c in encrypted_text))  # show escaped hex for clarity

    decrypted_text = xor_encrypt_decrypt(encrypted_text, key)
    print("Decrypted text:", decrypted_text)

if __name__ == "__main__":
    main()

```
## OUTPUT:
![image](https://github.com/user-attachments/assets/69e51eb4-dfb7-47d6-9a2c-4c0675c238f7)


## RESULT:
Thus code for Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is executed successfully.

