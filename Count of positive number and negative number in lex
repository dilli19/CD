%{
int pcount=0;
int ncount=0;
%}
%%
[0-9]+ {pcount++; printf("\n the number of positives are:%s",yytext);}
[-][0-9]+ {ncount++; printf("\n the number of negative are:%s",yytext);}
%%
int yywrap(void){}
int main()
{
printf("enter the numbers\n");
yylex();
printf("positives are=%d,"
          "negatives are=%d\n",
               pcount,ncount);
return 0;
}
