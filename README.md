# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:

~~~

#include <stdio.h>
#include <string.h>

int main()
{
    char url[200];
    char encrypted[200];
    char decrypted[200];
    int i, key = 5;

    printf("Enter URL: ");
    fgets(url, sizeof(url), stdin);

    url[strcspn(url, "\n")] = '\0';

    // Encryption
    for(i = 0; url[i] != '\0'; i++)
    {
        encrypted[i] = url[i] + key;
    }
    encrypted[i] = '\0';

    printf("\nEncrypted URL: %s", encrypted);

    // Decryption
    for(i = 0; encrypted[i] != '\0'; i++)
    {
        decrypted[i] = encrypted[i] - key;
    }
    decrypted[i] = '\0';

    printf("\nDecrypted URL: %s\n", decrypted);

    return 0;
}



~~~





# OUTPUT:
<img width="1545" height="716" alt="image" src="https://github.com/user-attachments/assets/c953890d-13c9-4cb8-9cda-bff7a06804dd" />


# RESULT:


