# Reserva-Teatro
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>

int main()
{

    int L[10][20]= {0}, l,c, coluna, fileira, b = 0;
    char le[10] = {'A','B','C','D','E','F','G','H','I','J'};
    char letra;
    char nome[80];

    do{

            printf("RESERVA DE LUGARES PARA: O FANTASMA DA OPERA, DIA 12/06 18HRS;\n");
            printf("====================================================================================\n");
            printf("MAPA DE LUGARES\n\n");
            printf("LUGARES VAGOS(0); LUGARES OCUPADOS(1); \n\n");
            printf("                          __________________________\n");
            printf("                         |                          |\n");
            printf("                         |           PALCO          |\n");
            printf("                         |                          |\n\n\n\n");
            printf("     1   2   3   4   5   6   7   8   9  ");
            printf("10  11  12  13  14  15  16  17  18  19  20");
            for (l = 0; l<10; l ++){
        printf("\n");
        printf("%c ",le[l]);
        for(c = 0; c<20; c++){
        printf(" |%2d", L[l][c]);}}
        printf("\n====================================================================================\n");
        printf("\nDIGITE O NUMERO DA POLTRONA(EX:A10):");
        scanf("%c%d", &letra, &coluna);
        fflush(stdin);
        letra = toupper(letra);
        while(letra < 65 || letra >74 || coluna>21 || coluna < 1){
            printf("POLTRONA INVALIDA!\n");
            printf("\nDIGITE OUTRO NUMERO PARA A POLTRONA(EX:A10):");
        scanf("%c%d", &letra, &coluna);
        fflush(stdin);
        letra = toupper(letra);
        }
        coluna = coluna - 1;
        if (L[fileira][coluna] == 1)
        do{
            printf("\nASSENTO JA OCUPADO!");
            printf("\nDIGITE OUTRO NUMERO PARA A POLTRONA(EX:A10):");
        scanf("%c%d", &letra, &coluna);
        fflush(stdin);
        letra = toupper(letra);
        while(letra < 65 || letra >74 || coluna>21 || coluna < 1){
            printf("POLTRONA INVALIDA!\n");
            printf("\nDIGITE OUTRO NUMERO PARA A POLTRONA(EX:A10):");
        scanf("%c%d", &letra, &coluna);
        fflush(stdin);
        letra = toupper(letra);
        }
        letra = toupper(letra);
        coluna = coluna - 1;
        }
        while (L[fileira][coluna] == 1);
        for(l=0; l<10; l++){
            if(letra == le[l]){
                fileira = l;
                L[fileira][coluna]++;}}
                fflush(stdin);
                printf("DIGITE O SEU NOME:");
                gets(nome);
                printf("==============================================================\n");
                printf("PARABENS SR(a) ");
                printf("%s",nome);
                printf(",\nO ASSENTO %c%d FOI RESERVADO COM SUCESSO PARA", letra, coluna = coluna + 1);
                printf("\nO FANTASMA DA OPERA, DIA 12/06 18HRS;\n");
                printf("==============================================================\n");

        system("pause");
        system("cls");}
        while(b == 0);




    printf("\n\n\n\n");
    return 0;
}
