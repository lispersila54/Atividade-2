# Atividade-2
Atividade 2 do Curso de Programação para Químicos 2021

QUESTÃO 1

#include <stdio.h>
#include <math.h> /* inclui essa função pois iremos utilizar seno no cálculo */
int main() // o clássico
{   
	/* declarei as variáveis que usarei */
    float i;
    float f;
    // um comando for para calcular todos os valores para o seno dentro desse intervalo
    for(i=0;i<=6.28;i=i+0.01){
        f=sin(i); // usei a função seno aqui
        printf("%.2f \n",f); // e aqui peço para imprimir o resultado apenas com duas casas decimais
    }
    return 0;
}

QUESTÃO 4

#include <stdio.h>
#include <math.h>
int main()
{
	// declarando as variáveis
	float x;
	float f,g,menor,maior;
    scanf("%f",&x); // peço o valo de entrada no qual vai ser usado para o cálculo
    //abaixo faço os cálculos para duas funções que chamei de f e g
    f= 1+ x/1 + x/2 + x/6; // facilitei o cálculo colocando logo o resultado da fatorial
    g=exp(x);
    // peço que apresente quais valores foram obtidos
    printf("%.2f \n",f);
    printf("%.2f \n",g);
    // abaixo começo as comparações mostrando se são iguais,diferentes e qual delas obteve o resultado maior e o menor
    if(f==g){
    	printf("iguais \n");
	}else {
		printf("diferentes \n");
	}
	maior=(f>g)?f:g;
	printf("Maior=%.2f \n",maior);
	menor=(f<g)?f:g;
	printf("Menor=%.2f \n",menor);    
    
    printf("Para valores próximos de 0 e distantes de 10, temos valores diferentes e com uma pequena distância entre eles, a partir que aumenta o valor de x, os valores continuam diferentes mas a distância entre eles aumentam.");

    return 0;
}

QUESTÃO 6

#include <stdio.h>
#include<stdlib.h>
int main()
{
	int i,maior,menor,j;
    int Numero[10];
    printf("Preencha esse array:\n");
    for(i=0;i<10;i++){
        scanf("%d",&Numero[i]);
    }
    
	for(i=1;i<10;i++){
		for(j=0;j<i;j++){
			if(Numero[i]>Numero[j]){
				maior = Numero[i];
				menor = Numero[j];
			} else{
				maior = Numero[j];
				menor = Numero[i];
			}
		}
	}
	printf(" \n o maior eh %d \n",maior);
	printf(" \n o menor eh %d \n",menor);	
    return 0;
}

QUESTÃO 8

#include <stdio.h>
#include <math.h>
int main()
{
    float x, Det;
    float Matriz[2][2];
    int i,j;
    scanf("%f",&x);
    for(i=1;i<=2;i++){
	    for(j=1;j>=i;j++){
            if(i==j){
                Matriz[i][j]=cos(x);
    
            }
            else if(i>j){
                Matriz[i][j]=-sin(x);
            }
            else{
                Matriz[i][j]=sin(x);
            }
	    }
    }
    Det=Matriz[1][2]*Matriz[2][1]-Matriz[1][1]*Matriz[2][2];
    printf("%.2f",&Det);
    return 0;
}
