%{
int macro=0 , header=0;
%}
%%
"#include" {header++;printf("\n header is:%s",yytext);}
"#define" {macro++;printf("\n macro is:%s",yytext);}
%%
int yywrap(){}
int main()
{
printf("enter the code\n");
yylex();
printf("no. of header files =%d,"
            "no.of macros =%d",
               header,macro);
return 0;
}
