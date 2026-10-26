# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

### DATE: 23-10-2026
### DEVELOPER: VAISHAK M
### REG NO: 212224040355

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
#include <string.h>

int main() {
    char message[100];
    int key, i;

    printf("Enter the plain text: ");
    fgets(message, sizeof(message), stdin);
    message[strcspn(message, "\n")] = 0;

    printf("Enter the key value: ");
    scanf(-"%d", &key);-

    for(i = 0; message[i] != '\0'; ++i) {
        char ch = message[i];
        if(ch >= 'a' && ch <= 'z') {
            ch = (ch - 'a' + key) % 26;
            if(ch < 0) ch += 26;
            ch = ch + 'a';
            message[i] = ch;
        }
        else if(ch >= 'A' && ch <= 'Z') {
            ch = (ch - 'A' + key) % 26;
            if(ch < 0) ch += 26;
            ch = ch + 'A';
            message[i] = ch;
        }
    }

    printf("Cipher Text: %s\n", message);
    return 0;
}
```
## OUTPUT:
<img width="1141" height="652" alt="image" src="https://github.com/user-attachments/assets/eb44c4f4-92ae-4503-bbb7-9671263302fb" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
