# Tic-Tac-Toe-game-with-different-levels
#include <stdio.h>
#include<conio.h>
char L[9]={'1','2','3','4','5','6','7','8','9'};
char M[16] = { 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j','k','l','m','n','o','p' };
char H[25] = { 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y'}; 
int k=0;
int end=1;
void Lboard()
{
    printf("\n\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\t\t|Tic Tac Toe|\n");
    printf("\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\tPlayer 1 (X)  -  Player 2 (O)\n");
    printf("\t\t\t\t\t___________________\n");
    printf("\t\t\t\t\t|     |     |     |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |\n", L[0], L[1], L[2]);

    printf("\t\t\t\t\t|_____|_____|_____|\n");
    printf("\t\t\t\t\t|     |     |     |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |\n", L[3], L[4], L[5]);

    printf("\t\t\t\t\t|_____|_____|_____|\n");
    printf("\t\t\t\t\t|     |     |     |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |\n", L[6], L[7], L[8]);
    printf("\t\t\t\t\t|_____|_____|_____|\n");
    printf("\t\t\t\t\t~~~~~~~~~~~~~~~~~~~\n");
}
void Mboard()
{
    printf("\n\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\t\t|Tic Tac Toe|\n");
    printf("\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\tPlayer 1 (X)  -  Player 2 (O)\n");
    printf("\t\t\t\t\t__________________________\n");
    printf("\t\t\t\t\t|     |     |     |      |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |\n", M[0], M[1], M[2],M[3]);

    printf("\t\t\t\t\t|_____|_____|_____|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |\n", M[4], M[5], M[6],M[7]);

    printf("\t\t\t\t\t|_____|_____|_____|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |\n", M[8], M[9], M[10],M[11]);
    printf("\t\t\t\t\t|_____|_____|_____|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |\n", M[12], M[13], M[14],M[15]);
    printf("\t\t\t\t\t|_____|_____|_____|______|\n");
    printf("\t\t\t\t\t~~~~~~~~~~~~~~~~~~~~~~~~~~\n");
}
void Hboard()
{
    printf("\n\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\t\t|Tic Tac Toe|\n");
    printf("\t\t\t\t\t\t~~~~~~~~~~~~~\n");
    printf("\t\t\t\t\tPlayer 1 (X)  -  Player 2 (O)\n");
    printf("\t\t\t\t\t_________________________________\n");
    printf("\t\t\t\t\t|     |     |     |      |      |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |  %c  |\n", H[0], H[1], H[2],H[3],H[4]);

    printf("\t\t\t\t\t|_____|_____|_____|______|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |      |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |  %c  |\n", H[5], H[6], H[7],H[8],H[9]);

    printf("\t\t\t\t\t|_____|_____|_____|______|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |      |\n");

    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |  %c  |\n", H[10], H[11], H[12],H[13],H[14]);
    printf("\t\t\t\t\t|_____|_____|_____|______|______|\n");
    printf("\t\t\t\t\t|     |     |     |      |      |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |  %c  |\n", H[15], H[16], H[17],H[18],H[19]);
    printf("\t\t\t\t\t|_____|_____|_____|______|______|\n");
     printf("\t\t\t\t\t|     |     |     |      |      |\n");
    printf("\t\t\t\t\t|  %c  |  %c  |  %c  |  %c   |  %c  |\n", H[20], H[21], H[22],H[23],H[24]);
    printf("\t\t\t\t\t|_____|_____|_____|______|______|\n");
    printf("\t\t\t\t\t~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\n");
}
void LgetInput()
{
    char ch;
    int i;
    printf("\n\t\t\t\t\t Enter the position: ");
    scanf("%c",&ch);
    if(k==0)
    {
    for(i=0;i<=8;i++){
        if(L[i]==ch)
        {
            L[i]='x';
            k=1;
            break;
        }
     } 
    }
    else{
      for(i=0;i<=8;i++){
        if(L[i]==ch)
        {
            L[i]='0';
            k=0;
            break;
        }
     } 
  }
}
void MgetInput()
{
    char ch;
    int i;
    printf("\n\t\t\t\t\t Enter the position: ");
    scanf("%c",&ch);
    if(k==0)
    {
    for(i=0;i<=15;i++){
        if(M[i]==ch)
        {
            M[i]='x';
            k=1;
            break;
        }
     } 
    }
    else{
      for(i=0;i<=15;i++){
        if(M[i]==ch)
        {
            M[i]='0';
            k=0;
            break;
        }
     } 
  }
}
void HgetInput()
{
    char ch;
    int i;
    printf("\n\t\t\t\t\t Enter the position: ");
    scanf("%c",&ch);
    if(k==0)
    {
    for(i=0;i<=24;i++){
        if(M[i]==ch)
        {
            M[i]='x';
            k=1;
            break;
        }
     } 
    }
    else{
      for(i=0;i<=24;i++){
        if(M[i]==ch)
        {
            M[i]='0';
            k=0;
            break;
        }
     } 
  }
}

int Lgameover(){
    if(L[0]=='x'&&L[1]=='x'&&L[2]=='x')
       return 1;
    else if(L[3]=='x'&&L[4]=='x'&&L[5]=='x') 
       return 1;
    else if(L[6]=='x'&&L[7]=='x'&&L[8]=='x') 
       return 1;
    else if(L[0]=='x'&&L[4]=='x'&&L[8]=='x') 
       return 1;
    else if(L[2]=='x'&&L[4]=='x'&&L[6]=='x') 
       return 1;
    else if(L[0]=='x'&&L[3]=='x'&&L[6]=='x') 
       return 1;   
    else if(L[1]=='x'&&L[4]=='x'&&L[7]=='x') 
       return 1;   
    else if(L[6]=='x'&&L[7]=='x'&&L[8]=='x') 
       return 1;
       
    else if(L[0]=='0'&&L[1]=='0'&&L[2]=='0')
       return 2;
    else if(L[3]=='0'&&L[4]=='0'&&L[5]=='0') 
       return 2;
    else if(L[6]=='0'&&L[7]=='0'&&L[8]=='0') 
       return 2;
    else if(L[0]=='0'&&L[4]=='0'&&L[8]=='0') 
       return 2;
    else if(L[2]=='0'&&L[4]=='0'&&L[6]=='0') 
       return 2;
    else if(L[0]=='0'&&L[3]=='0'&&L[6]=='0') 
       return 2;   
    else if(L[1]=='0'&&L[4]=='0'&&L[7]=='0') 
       return 2;   
    else if(L[6]=='0'&&L[7]=='0'&&L[8]=='0') 
       return 2;      
    else
       return 3;
}
int Mgameover(){
    if(M[0]=='x'&&M[1]=='x'&&M[2]=='x'&&M[3]=='x')
       return 1;
    else if(M[4]=='x'&&M[5]=='x'&&M[6]=='x'&&M[7]=='x') 
       return 1;
    else if(M[8]=='x'&&M[9]=='x'&&M[10]=='x'&&M[11]=='x') 
       return 1;
    else if(M[12]=='x'&&M[13]=='x'&&M[14]=='x'&&M[15]=='x') 
       return 1;
    else if(M[0]=='x'&&M[4]=='x'&&M[8]=='x'&&M[12]=='x') 
       return 1;
    else if(M[1]=='x'&&M[5]=='x'&&M[9]=='x'&&M[13]=='x') 
       return 1;
    else if(M[2]=='x'&&M[6]=='x'&&M[10]=='x'&&M[15]=='x') 
       return 1;   
    else if(M[3]=='x'&&M[7]=='x'&&M[11]=='x'&&M[15]=='x') 
       return 1;   
    else if(M[0]=='x'&&M[5]=='x'&&M[10]=='x'&&M[15]=='x') 
       return 1;
    else if(M[12]=='x'&&M[10]=='x'&&M[6]=='x'&&M[3]=='x') 
       return 1;
       
    else if(M[0]=='0'&&M[1]=='0'&&M[2]=='0'&&M[3]=='0')
       return 2;
    else if(M[4]=='0'&&M[5]=='0'&&M[6]=='0'&&M[7]=='0') 
       return 2;
    else if(M[8]=='0'&&M[9]=='0'&&M[10]=='0'&&M[11]=='0') 
       return 2;
    else if(M[12]=='0'&&M[13]=='0'&&M[14]=='0'&&M[15]=='0') 
       return 2;
    else if(M[0]=='0'&&M[4]=='0'&&M[8]=='0'&&M[12]=='0') 
       return 2;
    else if(M[1]=='0'&&M[5]=='0'&&M[9]=='0'&&M[13]=='0') 
       return 2;
    else if(M[2]=='0'&&M[6]=='0'&&M[10]=='0'&&M[15]=='0') 
       return 2;   
    else if(M[3]=='0'&&M[7]=='0'&&M[11]=='0'&&M[15]=='0') 
       return 2;   
    else if(M[0]=='0'&&M[5]=='0'&&M[10]=='0'&&M[15]=='0') 
       return 2;
    else if(M[12]=='0'&&M[10]=='0'&&M[6]=='0'&&M[3]=='0') 
       return 2;   
    else
       return 3;
}

int Hgameover(){
    if(H[0]=='x'&&H[1]=='x'&&H[2]=='x'&&H[3]=='x'&&H[4]=='x')
       return 1;
    else if(H[5]=='x'&&H[6]=='x'&&H[7]=='x'&&H[8]=='x'&&H[9]=='x') 
       return 1;
    else if(H[10]=='x'&&H[11]=='x'&&H[12]=='x'&&H[13]=='x'&&H[14]=='x') 
       return 1;
    else if(H[15]=='x'&&H[16]=='x'&&H[17]=='x'&&H[18]=='x'&&H[19]=='x') 
       return 1;
    else if(H[20]=='x'&&H[21]=='x'&&H[22]=='x'&&H[23]=='x'&&H[24]=='x') 
       return 1;   
    else if(H[0]=='x'&&H[6]=='x'&&H[12]=='x'&&H[18]=='x'&&H[24]=='x') 
       return 1;
    else if(H[3]=='x'&&H[8]=='x'&&H[13]=='x'&&H[18]=='x'&&H[23]=='x') 
       return 1;
    else if(H[2]=='x'&&H[7]=='x'&&H[12]=='x'&&H[17]=='x'&&H[22]=='x') 
       return 1;   
    else if(H[1]=='x'&&H[6]=='x'&&H[11]=='x'&&H[16]=='x'&&H[21]=='x') 
       return 1; 
    else if(H[0]=='x'&&H[5]=='x'&&H[10]=='x'&&H[15]=='x'&&H[20]=='x') 
       return 1;
    else if(H[4]=='x'&&H[8]=='x'&&H[12]=='x'&&H[16]=='x'&&H[20]=='x') 
       return 1;
    else if(H[4]=='x'&&H[9]=='x'&&H[14]=='x'&&H[19]=='x'&&H[24]=='x') 
       return 1;
       
       
    else if(H[0]=='0'&&H[1]=='0'&&H[2]=='0'&&H[3]=='0'&&H[4]=='0')
       return 1;
    else if(H[5]=='0'&&H[6]=='0'&&H[7]=='0'&&H[8]=='0'&&H[9]=='0') 
       return 1;
    else if(H[10]=='0'&&H[11]=='0'&&H[12]=='0'&&H[13]=='0'&&H[14]=='0') 
       return 1;
    else if(H[15]=='0'&&H[16]=='0'&&H[17]=='0'&&H[18]=='0'&&H[19]=='0') 
       return 1;
    else if(H[20]=='0'&&H[21]=='0'&&H[22]=='0'&&H[23]=='0'&&H[24]=='0') 
       return 1;   
    else if(H[0]=='0'&&H[6]=='0'&&H[12]=='0'&&H[18]=='0'&&H[24]=='0') 
       return 1;
    else if(H[3]=='0'&&H[8]=='0'&&H[13]=='0'&&H[18]=='0'&&H[23]=='0') 
       return 1;
    else if(H[2]=='0'&&H[7]=='0'&&H[12]=='0'&&H[17]=='0'&&H[22]=='0') 
       return 1;   
    else if(H[1]=='0'&&H[6]=='0'&&H[11]=='0'&&H[16]=='0'&&H[21]=='0') 
       return 1; 
    else if(H[0]=='0'&&H[5]=='0'&&H[10]=='0'&&H[15]=='0'&&H[20]=='0') 
       return 1;
    else if(H[4]=='0'&&H[8]=='0'&&H[12]=='0'&&H[16]=='0'&&H[20]=='0') 
       return 1;
    else if(H[4]=='0'&&H[9]=='0'&&H[14]=='0'&&H[19]=='0'&&H[24]=='0') 
       return 1;  
    else
       return 3;
}
void Lfinal()
{
    int var;
    var=Lgameover();
    if(var==1)
    {
        printf("\n\t\t\t\t\tPlayer one won");
        end=0;
    }
    else if(var==2)
    {
        printf("\n\t\t\t\t\tPlayer two won");
        end=0;
    }
    else;
}
void Mfinal()
{
    int var;
    var=Mgameover();
    if(var==1)
    {
        printf("\n\t\t\t\t\tPlayer one won");
        end=0;
    }
    else if(var==2)
    {
        printf("\n\t\t\t\t\tPlayer two won");
        end=0;
    }
    else;
}
void Hfinal()
{
    int var;
    var=Hgameover();
    if(var==1)
    {
        printf("\n\t\t\t\t\tPlayer one won");
        end=0;
    }
    else if(var==2)
    {
        printf("\n\t\t\t\t\tPlayer two won");
        end=0;
    }
    else;
}
int main()
{
    char p,c,r,s;
    printf("\n\n\n\n\n\n\n\n\n\t\t\t\t\t\t\t\t+++~~~~~~~~~~~~~~~~~~~~~~~~~~~~+++\n");
    printf("\t\t\t\t\t\t\t\t|     TIC       TAC       TOE    |\n");
    printf("\t\t\t\t\t\t\t\t+++~~~~~~~~~~~~~~~~~~~~~~~~~~~~+++\n\n\n");
    printf("\n\t\t\t\t\t-CHOOSE YOUR LEVEL:\n\n");
    printf("\t\t\t\t\t-> L for Low level\n\n\t\t\t\t\t-> M for Medium level\n\n\t\t\t\t\t-> H for High level\n\n");
    printf("\n\n\n\n\n\t\t\t\t\t\t\t\t    -(C) powered by MAN 'O' ISH \n\n");
    scanf("\t\t\t\t\t\t\t\t%c",&p);
    switch(p)
    {
        case 'L':
               label:
               Lboard();
               while(end){
               LgetInput();
               Lboard();
               Lfinal();
                }
               printf("\nDo you want to play again");
               printf("\nIf yes press y");
               fflush(stdin);
               scanf("%c",&c);
               if(c=='y'||c=='Y')
                 {
                    L[0]='1';L[1]='2'; L[2]='3'; L[3]='4'; L[4]='5'; L[5]='6'; L[6]='7'; L[7]='8'; L[8]='9';
                    k=0;end=1;
                    goto label;   
                 }
              break;
        case 'M': 
            BACK:
            Mboard();
             while(end){
              MgetInput();
              Mboard();
              Mfinal();
             }
              printf("\nDo you want to play again");
              printf("\nIf yes press y");
              fflush(stdin);
              scanf("%c",&r);
              if(r=='y'||r=='Y')
              {
                M[0]='a';M[1]='b'; M[2]='c'; M[3]='d'; M[4]='e'; M[5]='f'; M[6]='g'; M[7]='h'; M[8]='i'; M[9]='j';    
                M[10]='k';M[11]='l'; M[12]='m'; M[13]='n'; M[14]='o'; M[15]='p';
                k=0;end=1;
                goto BACK;   
              }
       
              break;
        case 'H':
                recap:
                Hboard();
                while(end){
                HgetInput();
                Hboard();
                Hfinal();
                }
                printf("\nDo you want to play again");
                printf("\nIf yes press y");
                fflush(stdin);
                scanf("%c",&s);
                if(s=='y'||s=='Y')
                  {
                  H[0]='a';H[1]='b'; H[2]='c'; H[3]='d'; H[4]='e'; H[5]='f'; H[6]='g'; H[7]='h'; H[8]='i'; H[9]='j';    
                  H[10]='k';H[11]='l'; H[12]='m'; H[13]='n'; H[14]='o'; H[15]='p'; H[16]='q'; H[17]='r'; H[18]='s'; H[19]='t';    
                  H[20]='u';H[21]='v'; H[22]='w'; H[23]='x'; H[24]='y';
                  k=0;end=1;
                  goto recap;   
                  }
              break;
    }
    return 0;
}



