# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xorCrypt(char msg[], char key[])
{
    int i, klen = strlen(key);
    for(i = 0; msg[i] != '\0'; i++)
    {
        msg[i] = msg[i] ^ key[i % klen];
    }
}

int main()
{
    char msg[] = "PRAVEENA";
    char key[] = "secretkey";

    printf("Original: %s\n", msg);
    xorCrypt(msg, key);
    printf("Encrypted: %s\n", msg);
    xorCrypt(msg, key);
    printf("Decrypted: %s\n", msg);

    return 0;
}
```
# OUTPUT:
 <img width="1465" height="844" alt="image" src="https://github.com/user-attachments/assets/5eaabc3e-05cf-4553-b0fd-d0ccc439cdbd" />

# RESULT:
using Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is successfully completed.


