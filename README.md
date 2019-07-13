#include<stdio.h>
#include<stdlib.h>

int main ()
{
	int jogada,opc,i,aux = 21,atualiza,auxpc = 1,pc,turn = 1;  
	
	printf ("***BEM VINDO AO JOGO DOS 21 PALITOS***\n");  //Tela inicial do Jogo
	printf ("***APERTE 1 PARA CONTINUAR***\n");
	scanf ("%d",&opc);
	 
	while (opc != 1)                                     // Caso a opção digitada para entrar no jogo seja diferente de 1;
	{
		printf ("***BEM VINDO AO JOGO DOS 21 PALITOS***\n");
	    printf ("***APERTE 1 PARA CONTINUAR***\n");
     	scanf ("%d",&opc);
	}
	
	if (opc == 1)               //Limpa a tela
	{
		system("cls");
	}


while (auxpc > 0)              // Repete a opção de seleção de palitos | auxpc é referente ao numero de palitos apos a jogada do computador;
{
	auxpc = 0;
	
	printf ("------------------------ Turno %d -------------------------\n",turn);
	
	printf ("Digite qnts palitos deseja retirar 1-2-3 ou 4 Palitos\n");
	scanf ("%d",&jogada);
	
	while ((jogada != 1) && (jogada != 2) && (jogada != 3) && (jogada != 4))  // Repete enquanto o numeros de palitos for difenrente aos estabelecidos nas regras do jogo 1-2-3-4 palitos
	{ 
		printf ("Digite qnts palitos deseja retirar 1-2-3 ou 4 Palitos\n");
    	scanf ("%d",&jogada);
	}
	
	if (jogada == 1)    // Caso o jogador 1 opte por retirar 1 palito
	{
		for (i = 0 ; i < aux - 1 ; i++)   // aux controla o numero inicial de palitos subtraindo o numero de palitos escolhido pelo jogador;
		{
			printf (" |");	
		}
		
		printf ("\n");
		
		aux = i;
		printf ("Apos jogada do jogador 1 sobraram: %d palitos\n",aux);
		printf ("\n");
	    
		printf ("Computador tirou: %d palitos\n",pc = 4);   // Jogada do computador;
		printf ("\n");
		
	  	
        auxpc = aux - pc;           // Variavel auxpc faz a subtração do numero de palitos retirados pelo jogador com os retirados pelo computador;
	  	aux = auxpc;                // Variavel aux recebe o valor da subtração de auxpc que é a atualização do numero de palitos disponivel
	  	
	    for ( i = 0 ; i < auxpc ; i++)     // Printa o novo tabuleiro apos os palitos retirados pelo jogador e pela maquina;
		{
			printf (" |");
			
		}
		printf ("\n");
	    printf ("Apos jogada do Computador sobraram: %d palitos \n",auxpc);   // Informar quantos palitos sobraram apos jogada da maquina;
	    printf ("\n");
	    
	    
	    printf ("\n");
	    
    if (aux == 1)                                                             // Caso aux seja igual a 1 o jogo para pois indica a derrota do jogador;
	{
		printf ("Jogador 1 perdeu Restou somente 1 Palito \n");
		printf ("\n");
		break;
	}
    }
    
    
    // A partir daqui todas as ações já executadas são repetidas ,porem agora realizando as ações caso a jogada do jogador seja igual a retirada de 2-3 ou 4 palitos;
    
    if ( jogada == 2)
    {
    		for (i = 0 ; i < aux - 2 ;i++)
		{
			printf (" |");	
		}
		
		printf ("\n");
		
		aux = i;
		printf ("Apos jogada do jogador 1 sobraram: %d palitos\n",aux);
	    printf ("\n");
	   
		printf ("Computador tirou: %d palitos\n",pc = 3);
		printf ("\n");	
		
        auxpc = aux - pc;
	  	aux = auxpc;
	  	
		for ( i = 0 ; i < auxpc ; i++)
		{
			printf (" |");
			
		}
		printf ("\n");
	    printf ("Apos jogada do Computador sobraram: %d palitos \n",auxpc);
	    
	    printf ("\n");
	    
    if (aux == 1)
	{
		printf ("Jogador 1 perdeu Restou somente 1 Palito \n");
		printf ("\n");
		break;
	}
	

	}
	
	 if ( jogada == 3)
    {
    		for (i = 0 ; i < aux - 3 ;i++)
		{
			printf (" |");	
		}
		
		printf ("\n");
		
		aux = i;
		printf ("Apos jogada do jogador 1 sobraram: %d palitos\n",aux);
		printf ("\n");
		  
		printf ("Computador tirou: %d palitos\n",pc = 2);	
		printf ("\n");
		
        auxpc = aux - pc;
	  	aux = auxpc;
	  	
		for ( i = 0 ; i < auxpc ; i++)
		{
			printf (" |");
			
		}
		printf ("\n");
	    printf ("Apos jogada do Computador sobraram: %d palitos \n",auxpc);
	    printf ("\n");
	    
	    printf ("\n");
	    
    if (aux == 1)
	{
		printf ("Jogador 1 perdeu Restou somente 1 Palito \n");
		printf ("\n");
		break;
    }
	
	
	}
	
	 if ( jogada == 4)
    {
    	for (i = 0 ; i < aux - 4 ;i++)
		{
			printf (" |");	
		}
		
	   	printf ("\n");
		
		aux = i;
		printf ("Apos jogada do jogador 1 sobraram: %d palitos\n",aux);
		printf ("\n");
		    
		printf ("Computador tirou: %d palitos\n",pc = 1);
		printf ("\n");
		
	  	
        auxpc = aux - pc;
	  	aux = auxpc;
	  	
		for ( i = 0 ; i < auxpc ; i++)
		{
			printf (" |");
			
		}
		printf ("\n");
	    printf ("Apos jogada do Computador sobraram: %d palitos \n",auxpc);
	    printf ("\n");
	    
	    printf ("\n");
	}
	
	if (aux == 1)
	{
		printf ("Jogador 1 perdeu Restou somente 1 Palito \n");
		printf ("\n");
		break;
	}
	
	turn++;          // Informa em qual turno esta a jogada;
	
}
	return 0;
}
