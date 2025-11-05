#include <stdio.h>
#include <stdlib.h>
#include <time.h>

char randomChar() {
    char chars[] = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*";
    return chars[rand() % (sizeof(chars) - 1)];
}

int main() {
    int length;
    srand(time(0));

    printf("Enter password length: ");
    scanf("%d", &length);

    printf("Generated Password: ");
    for (int i = 0; i < length; i++)
        printf("%c", randomChar());
    printf("\n");

    return 0;
}
