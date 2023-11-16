#include <stdio.h>

int countWhiteSpacesAndNewLines(const char *input) {
    int count = 0;
    int i;
    for (i = 0; input[i] != '\0'; i++) {
        if (input[i] == ' ' || input[i] == '\n') {
            count++;
        }
    }

    return count;
}

int main() {
    char input[100];

    printf("Enter a string: ");
    fgets(input, sizeof(input), stdin);

    int count = countWhiteSpacesAndNewLines(input);

    printf("Number of white spaces and new lines: %d\n", count);

    return 0;
}
