#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_LEN 1000

int main()
{
    char str [MAX_LEN];
    printf ("Enter a string:");
    fgets (str, MAX_LEN, stdin);
    char new_str [MAX_LEN];
    int j = 0;
    for (int i =0; i<=strlen(str);i++){
        if (i ==0 || str[i-1]== ' '){
            new_str[j++] = str[i];
        }
        else {
            new_str[j++] = tolower(str[i]);
        }
    }
    printf("Result: %s", new_str);
    return 0;

}
