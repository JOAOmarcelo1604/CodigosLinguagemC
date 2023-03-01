# CodigosLinguagemC
Resoluçoes de problemas em Linguagem C!




1)
#include <stdio.h>
int main() {
    int INDICE = 13, SOMA = 0, K = 0;

    while (K < INDICE) {
        K = K + 1;
        SOMA = SOMA + K;
    }

    printf("%d\n", SOMA);
    return 0;
}

2)
#include <stdio.h>
int main() {
    int num, a = 0, b = 1, c = 0, pertence = 0;
    printf("Digite um numero inteiro: ");
    scanf("%d", &num);
    
    while (c < num) {
        c = a + b;
        a = b;
        b = c;
    }

    if (c == num) {
        pertence = 1;
    }

    if (pertence) {
        printf("%d pertence a sequencia de Fibonacci.\n", num);
    } else {
        printf("%d nao pertence a sequencia de Fibonacci.\n", num);
    }

    return 0;
}

3)
#include <stdio.h>
#define TAMANHO_VETOR 31

int main() {
    double faturamento_diario[TAMANHO_VETOR] = {125.65, 0, 10.67, 56.34, 0, 0, 78.12, 43.21, 98.76, 54.32, 0, 12.34, 65.43, 87.65, 58.65, 43.21, 87.65, 0, 0, 21.43, 54.32, 98.76, 43.21, 76.54, 87.65, 43.21, 0, 0, 21.43, 54.32, 76.54};

    double minimo_faturamento = faturamento_diario[0];
    double maximo_faturamento = faturamento_diario[0];

    double somatorio = 0.0;
    int faturamento1 = 0;

   
    for (int i = 0; i < TAMANHO_VETOR; i++) {
        double faturamento = faturamento_diario[i];

        if (faturamento > 0.0) {
           faturamento1++;
            somatorio += faturamento;

            if (faturamento < minimo_faturamento) {
                minimo_faturamento = faturamento;
            }

            if (faturamento > maximo_faturamento) {
                maximo_faturamento = faturamento;
            }
        }
    }

    double media = somatorio / faturamento1;

  
    printf("Menor valor de faturamento: %.2f\n", minimo_faturamento);
    printf("Maior valor de faturamento: %.2f\n", maximo_faturamento);
    printf("Número de dias com faturamento superior à média mensal: %d\n", faturamento1);
    
    return 0;
}

4)
#include <stdio.h>
int main() {
    float sp = 67.83643;
    float rj = 36.67866;
    float mg = 29.22988;
    float es = 27.16548;
    float outros = 19.84953;
    
    float total = sp + rj + mg + es + outros;
    
    float percentual_sp = (sp / total) * 100;
    float percentual_rj = (rj / total) * 100;
    float percentual_mg = (mg / total) * 100;
    float percentual_es = (es / total) * 100;
    float percentual_outros = (outros / total) * 100;
    
    printf("Percentual de representacao por estado:\n");
    printf("SP: %.2f%%\n", percentual_sp);
    printf("RJ: %.2f%%\n", percentual_rj);
    printf("MG: %.2f%%\n", percentual_mg);
    printf("ES: %.2f%%\n", percentual_es);
    printf("Outros: %.2f%%\n", percentual_outros);
    
    return 0;
}

5)
#include <stdio.h>
#include <string.h>

int main() {
    char string[100];
    int a, x;
    
 
    printf("Digite uma palavra: ");
    fgets(string, 100, stdin);
    

    string[strcspn(string, "\n")] = 0;
    
  
    for (a = 0, x = strlen(string) - 1; a < x; a++, x--) {
        char temp = string[a];
        string[a] = string[x];
        string[x] = temp;
    }
    printf("Palavra invertida: %s\n", string);
    
    return 0;
}

