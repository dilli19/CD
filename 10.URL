%{
%}
%%
"https"|"ftp"[//][a-zA-Z]{3}[.][a-zA-Z]+".""com" {printf("valid URL");}
[0-9]+ {printf("invalid URL");}
%%
int yywrap(void){}
int main(){
printf("enter : ");
yylex();
printf("\n");
return 0;
}
