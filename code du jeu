#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void init_carte(int map[20][20]) {
    int i, j, s ;
    for(i=0; i<20; i++) {
        for(j=0; j<20; j++) {
            map [i][j] = 0 ;
            }
        }
    for(s=0;s<20;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 8;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<50;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 3;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<20;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 2;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<20;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 1;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<2;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 4;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<8;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 5;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<2;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] = 6;
            }
        else{
            s= s-1 ;
            }
        }
    for(s=0;s<30;s++) {
        i=(rand()%20)+0;
        j=(rand()%20)+0;
        if((map [i][j] == 0) && ((i != 0) || (j != 0))) {
            map [i][j] =7;
            }
        else{
            s= s-1 ;
            }
        }
    }




void affiche_carte(int map[20][20],int perso[2]) {
    int i, j ;
    system("clear");
    printf("\n") ;
    for(i=0; i<42; i++) {
        printf("─");
        }
    printf("\n") ;
    for(i=0; i<20; i++) {
    printf("│");
        for(j=0 ; j < 20; j++) {
            if((i== perso[0])&&(j==perso[1])) {
                printf("X") ;
                }
            else if(map[i][j]==0){
                printf(" ") ;
                }
    else if(map[i][j]==1){
                printf("f") ;
                }
            else if(map[i][j]==2){
                printf("Y") ;
                }
            else if(map[i][j]==3){
                printf("G") ;
                }
            else if(map[i][j]==4){
                printf("k") ;
                }
            else if(map[i][j]==5){
                printf("☭") ;
                }
            else if(map[i][j]==6){
                printf("#") ;
                }
            else if(map[i][j]==7){
                printf(" ") ;
                }
            else if(map[i][j]==8){
                printf("♌") ;
                }
            printf(" ") ;
            }
    printf("│");
        printf("\n") ;
        }
    for(i=0; i<42; i++){
        printf("─");
        }
    printf("\n") ;

    }

int deplacement_perso(int move, int perso[2]){
    do {
        printf(" 8-4-2-6-0(arret)\n") ;
        scanf("%d", &move) ;
        switch (move) {
            case 8 : perso [0]--;
                if (perso [0] == -1 ) {
                    perso [0] = perso [0] +1 ;
                    }
                break ;
            case 4 : perso [1]--;
                if (perso [1] == -1 ) {
                    perso [1] = perso[1] + 1;
                    }
                break ;
            case 2 : perso [0]++;
                if (perso [0] == 20 ) {
                    perso [0] = perso [0] -1;
                    }
                break ;
            case 6 : perso [1]++;
                if (perso [1] == 20  ) {
                    perso [1] = perso[1] - 1;
                    }
                break;
            case 0 :;
                break;
            default : printf("\nEntrée incorrecte, recommence!\n") ;
                break;
            }
    }while (move!=2 && move!=4 && move!=8 && move!=6 && move!= 0) ;
    return move ;
    }

int main(){
    srand(time(NULL));
    int money, life, key, quit, move, partie ;
    int perso[2] ;
    int map[20][20] ;
    perso[0]=0;
    perso[1]=0;
    quit = 1;
    partie=1;
    printf("\nBienvenue dans le jeu!\n Voulez vous commencer une partie? (1=oui, 0=non)\n") ;
    scanf("%d", &partie) ;
    if (partie== 1) {
        while(quit!=0) {
                printf("\n La partie va commencer!\n Pour gagner, tu devras récolter 10 pièces( ☭)!\nIl y a des monstres, symbolisé par un :♌, des arbres: Y, des fleurs: f, des clés: k et des cadenas: # (ainsi que des pièges, mais ils sont cachés :p) \n") ;

                perso[0]=0;
                perso[1]=0;
                move= 0 ;
                key = 0;
                life=10;
        partie=1;
                money=0;
            init_carte(map) ;
            while(partie == 1){
                affiche_carte(map, perso) ;
                printf("vie=%d  clé=%d pieces=%d\n", life, key, money) ;
                    move = deplacement_perso(move, perso) ;
        if (move==0) {
            partie=0;
            }
                    if(map [perso[0]] [perso[1]] == 3) {
                        switch (move) {
                        case 8 : perso[0] ++ ;
                                break ;
                        case 4 : perso [1] ++;
                                break;
                        case 2 : perso[0] --;
                                break;
                        case 6 : perso[1] -- ;
                            break;
                        }
                    }
        if(map [perso[0]] [perso[1]] == 2){
            switch (move) {
                        case 8 : perso[0] ++ ;
                            break ;
                        case 4 : perso [1] ++;
                            break;
                        case 2 : perso[0] --;
                            break;
                        case 6 : perso[1] -- ;
                            break;
                        }
        }
                if(map[perso[0]][perso[1]] == 8) {
                    life=life-1 ;
                    }
        if(map[perso[0]][perso[1]] == 7) {
                    life=life-1 ;
        printf("\nTu as marcher sur un piège, tu perd une vie\n");

                    }
                if(map [perso[0]] [perso[1]] == 5 ) {
                    money= money+1;
                    }
                if(map [perso[0]] [perso[1]] == 4 ) {
                    key=key+1;
                    }
                if(map [perso[0]] [perso[1]] == 6 ) {
                    if(key!=0){
                        money =money+1;
                        key=key-1;
                        }
                    else{
                        switch (move) {
                            case 8 : perso[0] ++ ;
                                break ;
                            case 4 : perso [1] ++;
                                break;
                            case 2 : perso[0] --;
                                break;
                            case 6 : perso[1] -- ;
                                break;
                            }
                        printf("\n il te faut la clé!\n");

                        }
                    }
                map [perso[0]] [perso[1]] = 0 ;
                if(life==0){
                    printf("Tu n’as plus de vie, tu as perdu !\n");
            partie=0;
                    }
                if(money==10) {
                    printf("Tu as trouvé toutes les pièces ! Tu as gagné !\n");
            partie=0;
                    }
                }
            printf("\n Recommencer?(1 oui, 0 non)\n");
            scanf("%d", &quit);
            }
            printf("\n Fin du jeu !\n") ;
        }
    return 0;
    }
