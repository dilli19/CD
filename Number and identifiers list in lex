%{
#include <stdio.h>
%}

%%

[0-9]+          { printf("Number: %s\n", yytext); }

.|\n            { /* Ignore other characters */ }

%%

int main() {
    yylex();
    return 0;
}
