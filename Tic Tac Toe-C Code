/*
AUTHOR: AJ
DATE: 16-10-20
PROGRAM: TIC-TAC-TOE
*/
#include <stdio.h>
#include <stdlib.h>

// DISPLAY THE 3X3 BOARD
void display(char mat[3][3])
{
    int i,j;
    printf("\n");
    for (i=0;i<3;i++)
    {
        for (j=0;j<3;j++)
            printf("%c\t",mat[i][j]);
        printf("\n\n");
    }
}
// CHECKING IF ANY PLAYER WON THE GAME AFTER EVERY MARKING
int check(char mat[3][3])
{
    int i;
    // CHECKING THE TWO DIAGONALS
    if ( (mat[0][0]!='*' && mat[0][0]==mat[1][1] && mat[1][1]==mat[2][2] ) || (mat[0][2]!='*' && mat[0][2]==mat[1][1] && mat[2][0]==mat[1][1] ))
    {
        printf("Congratulations!! You've won!!\n\n");
        return 1;
    }
    // CHECKING THE ROWS
    for (i=0;i<3;i++)
        if (mat[i][0]!='*' && mat[i][0]==mat[i][1] && mat[i][1]==mat[i][2])
    {
        printf("Congratulations!! You've won!!\n\n");
        return 1;
    }
    //CHECKING THE COLUMNS
    for (i=0;i<3;i++)
        if (mat[0][i]!='*' && mat[0][i]==mat[1][i] && mat[1][i]==mat[2][i])
    {
        printf("Congratulations!! You've won!!\n\n");
        return 1;
    }
    return 0;
}
int main(void)
{

    printf("Let's play a game of tic-tac-toe!\n\n");
    int i,j,steps;
    char mat[3][3],c;
    // INITIALIZING THE GAME BOARD
    for (i=0;i<3;i++)
        for(j=0;j<3;j++)
            mat[i][j]='*';
    display(mat);

    printf("Let me tell you how to play!\nYou have a 3x3 board above where the (i,j)th position denotes the ith row and jth column of the board!\nThere are two markers-\"x\" and \"o\".\nThe player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row is the winner.\n\nLet's begin!\nDo you want to go first? (y\\n):\t");
    scanf("%c",&c);
    k:
    steps=1;
    printf("Enter your name:\t");
    char opponent_name[20], opponent_marker;
    scanf("%s",opponent_name);
    printf("Enter your marker:\t");
    fflush(stdin);
    scanf("%c",&opponent_marker);

    if (c=='y')
    {
        printf("Enter your position, %s, in i,j format:\t",opponent_name);
        scanf("%d,%d",&i,&j);
        mat[i-1][j-1]=opponent_marker;
        display(mat);
        while (steps<=4)
        {
            printf("Enter your position, AJ, in i,j format:\t"); // BY DEFAULT , PLAYER 2 IS THE AUTHOR-CAN BE CHANGED
            scanf("%d,%d",&i,&j);
            if (mat[i-1][j-1]!='*')
            {
                printf("Position already in use! Please enter a correct position in i,j format:\t");
                scanf("%d,%d",&i,&j);
            }
            mat[i-1][j-1]=opponent_marker=='x'?'o':'x';
            display(mat);
            if (check(mat)==1)
            {
                printf("Do you want to play again?(y\\n):\t");
                fflush(stdin);
                scanf("%c",&c);
                if (c=='y')
                {
                    for (i=0;i<3;i++)
                        for(j=0;j<3;j++)
                            mat[i][j]='*';
                    display(mat);
                    goto k;
                }
            else return 0;
            }
            printf("Enter your position, %s, in i,j format:\t",opponent_name);
            scanf("%d,%d",&i,&j);
            if (mat[i-1][j-1]!='*')
            {
                printf("Position already in use! Please enter a correct position in i,j format:\t");
                scanf("%d,%d",&i,&j);
            }
            mat[i-1][j-1]=opponent_marker;
            display(mat);
            if (check(mat)==1)
            {
                printf("Do you want to play again?(y\\n):\t");
                fflush(stdin);
                scanf("%c",&c);
                if (c=='y')
                {
                    for (i=0;i<3;i++)
                        for(j=0;j<3;j++)
                            mat[i][j]='*';
                    display(mat);
                    goto k;
                }
                else return 0;
            }
            steps++;
        }
    }
    else
        {
            printf("Enter your position, AJ, in i,j format:\t");
            scanf("%d,%d",&i,&j);
            if (mat[i-1][j-1]!='*')
            {
                printf("Position already in use! Please enter a correct position in i,j format:\t");
                scanf("%d,%d",&i,&j);
            }
            mat[i-1][j-1]=opponent_marker=='x'?'o':'x';
            display(mat);
            while (steps<=4)
        {
            printf("Enter your position, %s, in i,j format:\t",opponent_name);
            scanf("%d,%d",&i,&j);
            mat[i-1][j-1]=opponent_marker;
            display(mat);
            if (check(mat)==1)
            {
                printf("Do you want to play again?(y\\n):\t");
                fflush(stdin);
                scanf("%c",&c);
                if (c=='y')
                {
                    for (i=0;i<3;i++)
                        for(j=0;j<3;j++)
                            mat[i][j]='*';
                    display(mat);
                    goto k;
                }
                else return 0;
            }
            printf("Enter your position, AJ, in i,j format:\t");
            scanf("%d,%d",&i,&j);
            if (mat[i-1][j-1]!='*')
            {
                printf("Position already in use! Please enter a correct position in i,j format:\t");
                scanf("%d,%d",&i,&j);
            }
            mat[i-1][j-1]=opponent_marker=='x'?'o':'x';
            display(mat);
            if (check(mat)==1)
            {
                printf("Do you want to play again?(y\\n):\t");
                fflush(stdin);
                scanf("%c",&c);
                if (c=='y')
                {
                    for (i=0;i<3;i++)
                        for(j=0;j<3;j++)
                        mat[i][j]='*';
                    display(mat);
                    goto k;
                }
                else return 0;
            }
            steps++;
        }
        }
    printf("Game over!!\nDo you want to play again?(y\\n):\t");
    fflush(stdin);
    scanf("%c",&c);
    if (c=='y')
    {
        for (i=0;i<3;i++)
            for(j=0;j<3;j++)
                mat[i][j]='*';
        display(mat);
        goto k;
    }
    else return 0;
}
