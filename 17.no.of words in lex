%{
int char_count = 0;
int word_count = 0;
int line_count = 0;
%}

%%
[a-zA-Z]+    { word_count++; }
.            { char_count++; }

\n           { line_count++; }
%%

int yywrap() {
    return 1;  
}

int main() {
    printf("enter :");
    yylex();
    printf("Character count: %d\n", char_count);
    printf("Word count: %d\n", word_count);
    printf("Line count: %d\n", line_count);
    return 0;
}
