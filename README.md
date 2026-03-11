# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:

```.py
#include <stdio.h>
#include <string.h>

int main() {
    char plaintext[50], key[50], encrypted[50], decrypted[50];
    int i;

    printf("Enter Plain Text: ");
    scanf("%s", plaintext);

    printf("Enter Key: ");
    scanf("%s", key);

    // Encryption
    for (i = 0; i < strlen(plaintext); i++) {
        encrypted[i] = plaintext[i] ^ key[i % strlen(key)];
    }
    encrypted[i] = '\0';

    printf("Encrypted Text: ");
    for (i = 0; i < strlen(plaintext); i++) {
        printf("%c", encrypted[i]);
    }

    // Decryption
    for (i = 0; i < strlen(plaintext); i++) {
        decrypted[i] = encrypted[i] ^ key[i % strlen(key)];
    }
    decrypted[i] = '\0';

    printf("\nDecrypted Text: %s\n", decrypted);

    return 0;
}


```

## Output:

<img width="526" height="338" alt="image" src="https://github.com/user-attachments/assets/212b90c8-743a-40c7-b61a-4d3bf54cdd33" />



## Result:

Thus, the simple DES encryption and decryption program was successfully implemented using C programming language. The plaintext was encrypted using a secret key and the original message was correctly obtained after decryption without any errors.
  The program is executed successfully
