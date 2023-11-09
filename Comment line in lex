%{
int c=0;
%}
%%
"//"|"/*"[a-zA-Z] {c++;printf("\n %s is a comment line \n",yytext);}
.+ {printf("The Given input is  not comment line");}
%%
int yywrap(){}
int main()
{
printf("enter : ");
yylex();
printf("\nno of comments:%d",c);
return 0;
}
