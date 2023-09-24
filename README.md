# Produto-de-Matrizes-em-C
Multiplicação de duas matrizes 3x3(pode mudar), em C.
Leia o codigo inteiro.



1. Codigo com os valores das matrizes pre-definidas.
#include <stdio.h>
int main() {
	
	//Declaro as matrizes com seus valores ja implementados.
    int matriz1[3][3]={{1,2,3},{1,2,3},{1,2,3}}, matriz2[3][3]={{1,2,3},{1,2,3},{1,2,3}}, matriz_resultante[3][3];
    int i = 0, k = 0, j = 0, z = 0;
			
do{

	//Uso tres "for" para que um dos valores nao mude durante o calculo.
	//Assim perseguind toda a coluna ou linha da matriz com um mesmo valor.
    for(k=0; k<z; k++){
   		  for(i=0; i<3; i++){
		    	for(j=0; j<3; j++){
             matriz_resultante[i][j]= (matriz1[j][k]*matriz2[k][j])+(matriz1[j][k+1]*matriz2[k+1][j])+(matriz1[j][k+2]*matriz2[k+2][j]);
    	//Depois apenas realizo os calculos mudando os valores de linha e coluna.
      // Esses valores com "+1" servem para eu manipular a equaçao, e como os valores estao mudando, eu nao perco algo.
		
}
    	}
        		}
                z+=1;
}while(z<3); //Faço um "do while" para repetir o calculo 3 vezes. 

   //Agora imprime...             	
    printf("Produto das Matrizes:\n");            	
           	for(int i=0; i<3; i++){
				for(int j=0; j<3; j++){
					printf("%i ", matriz_resultante[i][j]);
					}
					printf("\n");
				}
}

2. Codigo com leitura dos valores das matrizes .

#include <stdio.h>
int main() {
	//Declaro as matrizes.
    int matriz1[3][3], matriz2[3][3], matriz_resultante[3][3], i = 0, j = 0, k = 0,  z=0;
    
	printf("Digite a Primeira Matriz:\n");
	
    	for(i = 0; i < 3; i++){
			for(j = 0; j < 3; j++){
					scanf("%i ", &matriz1[i][j]);
			}
		}  //Leio a primeira matriz.
	
		printf("Digite a Segunda Matriz:\n");
		
		for(i = 0; i < 3; i++){
			for(j = 0; j < 3; j++){
					scanf("%i ", &matriz2[i][j]);
			}
		}  //Leio a segunda matriz.
		
    printf("Suas Matrizes:\n");
    
    	for(i=0; i<3; i++){
			for(j=0; j<3; j++){
					printf("%i ", matriz1[i][j]);
			}
					printf("\n");
		}
		
		printf("\n");
		
		for(i=0; i<3; i++){
			for(j=0; j<3; j++){
					printf("%i ", matriz2[i][j]);
			}
					printf("\n");
		}  //Mostro as matrizes.
		
		printf("\n");
		
		//Mesma calculo de antes...
    do{ //Uso o "do while" para repetir o calculo tres vezes, porque eh uma matriz 3x3.

    // E uso tres "for", o primeiro para o valor nao mudar na hora do calculo, e os outros dois para percorrer a matriz.
    	for(k=0; k<z; k++){
   		    for(i=0; i<3; i++){
				for(j=0; j<3; j++){
        matriz_resultante[i][j]= (matriz1[j][k]*matriz2[k][j])+(matriz1[j][k+1]*matriz2[k+1][j])+(matriz1[j][k+2]*matriz2[k+2][j]);
                                // Esses valores com "+1" servem para eu manipular a equaçao, e como os valores estao mudando, eu nao perco algo.
        }
        	}
        		}
                z+=1;
                	}while(z<3);
                	
                	// Resultado...
                	printf("Produto das Matrizes:\n");
                	for(i=0; i<3; i++){
						for(j=0; j<3; j++){
					printf("%i ", matriz_resultante[i][j]);
					}
					printf("\n");
				}
}

//Fim.
