# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <stdlib.h>
void caesarEncrypt(char *text, int key) {
for (int i = 0; text[i] != '\0'; i++) { char c = text[i];
if (c >= 'A' && c <= 'Z') {
text[i] = ((c - 'A' + key) % 26 + 26) % 26 + 'A';
}
else if (c >= 'a' && c <= 'z') {
text[i] = ((c - 'a' + key) % 26 + 26) % 26 + 'a';
}
}
}
The program is executed successfully
Releases
No releases published
Packages
void caesarDecrypt(char *text, int key) {
caesarEncrypt(text, -key);
}
int main() {
char message[100];
int key;
printf("Enter the message to encrypt: ");
fgets(message, sizeof(message), stdin);
printf("Enter the Caesar Cipher key (an integer): ");
scanf("%d", &key);
caesarEncrypt(message, key);
printf("Encrypted Message: %s", message);
caesarDecrypt(message, key);
printf("Decrypted Message: %s", message);
return 0;
}
```
## OUTPUT:
<img width="776" height="140" alt="image" src="https://github.com/user-attachments/assets/bfc06938-2cdd-4d4e-8292-7d35009fdadf" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
