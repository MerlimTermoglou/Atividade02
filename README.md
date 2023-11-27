# Atividade02

#include <stdio.h>



int main(){
    FILE *even, *odds;
    int n = 10;
    size_t k = 0;

    even = fopen("even.txt", "w");
    odds = fopen("odds.txt", "w");

    for(k = 1; k < n + 1; k++){
        k%2==0 ? fprintf(even, "\t%5d\n", k)
                : fprintf(odds, "\t%5d\n", k);
    }
    fclose(even);
    fclose(odds);

    return 0;
}
-------------------

#include <stdio.h>

int main() {
    int a = 20;
    int b = -5;

    
    
    if (a = 20 && b == -5) { //mudando os sinais != para =  
        printf("Eu serei impresso!\n"); 
    }

    return 0;
}

-----

#include <stdio.h>


int print(int i) {
    if (i == 20) {
        printf("Mostrando a função para %d\n", i); 
        return 1; 
    } else  { 
        printf("Não mostrando a função para %d\n", i);
        return 0;
    }
}
    // importante ter colocado o else para chamar os ifs abaixo

int main(void) {
    int a = 20; // se mudar este numero a vai ser alternado os carinhas de baixo

   
    if ((a != 20) && print(a)) {           
        printf("Eu não serei mostrado!\n");
    }

    
    if ((a == 20) && print(a)) {
        printf("Eu vou ser mostrado!\n");
    }

    return 0;
}

----
#include <stdio.h>

int main() 
{
    char sentence[] = "data : 06-06-2012"; 
    char str[50]; 
    int day, month, year; 

    
    sscanf(sentence, "%s : %2d-%2d-%4d", str, &day, &month, &year); // o erro estava na variavel year; n foi colocada aqui
    
   
    printf("%s -> %02d-%02d-%4d\n", str, day, month, year);
               
    return 0;
}

-----
