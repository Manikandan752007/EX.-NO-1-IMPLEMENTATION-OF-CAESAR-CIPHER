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
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
void encrypt(char a[] , int key)
{
 for(int i = 0 ; a[i] != '\0' ; i++)
 {
 char ch = a[i];
 if(isalpha(ch))
 {
 char base = isupper(ch) ? 'A' : 'a';
 a[i] = (ch - base + key) % 26 + base;
 }
 }
}
void decrypt(char a[] , int key)
{
 for(int i = 0 ; a[i] != '\0' ; i++)
 {
 char ch = a[i];
 if(isalpha(ch))
 {
 char base = isupper(ch) ? 'A' : 'a';
 a[i] = (ch - base - key + 26) % 26 + base;
 }
 }
}
int main()
{
 char a[100];
 int key,choice;
 printf("Enter the text to encrypt or decrypt : ");
 fgets(a,100,stdin);
 printf("Enter the key : ");
 scanf("%d",&key);
 encrypt(a,key);
 printf("Encrypted text : %s",a);
 decrypt(a,key);
 printf("Decrypted text : %s",a);
}
```
## OUTPUT:
<img width="1687" height="776" alt="image" src="https://github.com/user-attachments/assets/172d9bc3-2ae6-47e7-a46b-8720e7f6c69b" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
