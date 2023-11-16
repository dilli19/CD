#include <stdio.h>
#include <ctype.h>
#include <stdbool.h>

void remove_comments(char *code) {
    enum {
        CODE,
        COMMENT_LINE,
        COMMENT_BLOCK
    } state = CODE;

    char *p = code;
    char *q = code;

    while (*p != '\0') {
        if (state == CODE) {
            if (*p == '/' && *(p + 1) == '/') {
                state = COMMENT_LINE;
                p += 2;
            } else if (*p == '/' && *(p + 1) == '*') {
                state = COMMENT_BLOCK;
                p += 2;
            } else {
                *q++ = *p++;
            }
        } else if (state == COMMENT_LINE) {
            if (*p == '\n') {
                state = CODE;
            }
            p++;
        } else if (state == COMMENT_BLOCK) {
            if (*p == '*' && *(p + 1) == '/') {
                state = CODE;
                p += 2;
            } else {
                p++;
            }
        }
    }

    *q = '\0';
}

void tokenize(char *code) {
    char *p = code;

    while (*p != '\0') {

        if (isspace(*p)) {
            p++;
            continue;
        }

        if (isalpha(*p) || *p == '_') {
            char identifier[256] = "";
            int i = 0;
            while (isalnum(*p) || *p == '_') {
                identifier[i++] = *p++;
            }
            printf("Identifier/Keyword: %s\n", identifier);
            continue;
        }

        if (isdigit(*p)) {
            int number = 0;
            while (isdigit(*p)) {
                number = number * 10 + (*p++ - '0');
            }
            printf("Numeric Literal: %d\n", number);
            continue;
        }

        if (*p == '"' || *p == '\'') {
            char delimiter = *p++;
            while (*p != delimiter) {
                printf("%c", *p++);
            }
            printf("\n");
            p++;
            continue;
        }


        printf("Non-Word Character: %c\n", *p++);
    }
}

int main() {
    char code[] = "#include <stdio.h>\n\nint main() {\n    // Print Hello, World!\n    printf(\"Hello, World!\\n\");\n    return 0;\n}";

    remove_comments(code);

    tokenize(code);

    return 0;
}
