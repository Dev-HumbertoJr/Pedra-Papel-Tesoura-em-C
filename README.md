#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    short int Escolha_Jogador1, Escolha_Computador, Escolha_Jogador2, opcao;

    srand(time(0));

    printf("***Jogo de Jokenpô***\n");
    printf("Escolha uma opção\n");
    printf("1. Jogar contra o computador\n");
    printf("2. Jogar contra outro jogador\n");
    printf("Escolha: ");
    scanf("%hd", &opcao);

    switch (opcao)
    {
    case 1:

        printf("\n1. Pedra\n");
        printf("2. Papel\n");
        printf("3. Tesoura\n");
        printf("Escolha: ");
        scanf("%hd", &Escolha_Jogador1);

        switch (Escolha_Jogador1)
        {
        case 1:
            printf("\nJogador: Pedra - ");
            break;

        case 2:
            printf("\nJogador: Papel - ");
            break;

        case 3:
            printf("\nJogador: Tesoura - ");
            break;

        default:
            printf("!!Opção inválida!!\n");
            return 0;
        }

        Escolha_Computador = rand() % 3 + 1;

        switch (Escolha_Computador)
        {
        case 1:
            printf("Computador: Pedra\n");
            break;

        case 2:
            printf("Computador: Papel\n");
            break;

        case 3:
            printf("Computador: Tesoura\n");
            break;
        }

        if (Escolha_Jogador1 == Escolha_Computador)
        {
            printf("### Empate! ###");
        }
        else if ((Escolha_Jogador1 == 1 && Escolha_Computador == 3) ||
                 (Escolha_Jogador1 == 2 && Escolha_Computador == 1) ||
                 (Escolha_Jogador1 == 3 && Escolha_Computador == 2))
        {
            printf("### Você venceu! ###");
        }
        else
        {
            printf("### Você perdeu! ###");
        }

        break;

    case 2:

        printf("\nJogador 1\n");
        printf("1. Pedra\n");
        printf("2. Papel\n");
        printf("3. Tesoura\n");
        printf("Faça o seu jogo: ");
        scanf("%hd", &Escolha_Jogador1);

        printf("\nJogador 2\n");
        printf("1. Pedra\n");
        printf("2. Papel\n");
        printf("3. Tesoura\n");
        printf("Faça o seu jogo: ");
        scanf("%hd", &Escolha_Jogador2);

        switch (Escolha_Jogador1)
        {
        case 1:
            printf("\nJogador 1: Pedra - ");
            break;

        case 2:
            printf("\nJogador 1: Papel - ");
            break;

        case 3:
            printf("\nJogador 1: Tesoura - ");
            break;

        default:
            printf("!!Opção inválida!!\n");
            return 0;
        }

        switch (Escolha_Jogador2)
        {
        case 1:
            printf("Jogador 2: Pedra\n");
            break;

        case 2:
            printf("Jogador 2: Papel\n");
            break;

        case 3:
            printf("Jogador 2: Tesoura\n");
            break;

        default:
            printf("!!Opção inválida!!\n");
            return 0;
        }

        if (Escolha_Jogador1 == Escolha_Jogador2)
        {
            printf("### Empate! ###");
        }
        else if ((Escolha_Jogador1 == 1 && Escolha_Jogador2 == 3) ||
                 (Escolha_Jogador1 == 2 && Escolha_Jogador2 == 1) ||
                 (Escolha_Jogador1 == 3 && Escolha_Jogador2 == 2))
        {
            printf("### Jogador 1 venceu! ###");
        }
        else
        {
            printf("### Jogador 2 venceu! ###");
        }

        break;

    default:
        printf("Opção inválida!\n");
        break;
    }

    return 0;
}
