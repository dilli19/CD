%{
int html=0;
%}
%%
"<"[a-zA.Z.]+">" {html++;printf("%s ia a htmal tag",yytext);}
.;
%%
int yywrap(){}
int main()
{
yylex();
printf("number of html tags=%d\n",html);
return 0;
}
