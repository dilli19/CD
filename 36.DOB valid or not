%{
#include <stdio.h>
%}
%%
[0-9]{1,2}-[0-9]{1,2}-[0-9]{4} { printf("Valid date of birth\n"); }
.+ { printf("Invalid date of birth\n"); }

%%
int yywrap(void){}
int main() {
yylex();
return 0;
}
