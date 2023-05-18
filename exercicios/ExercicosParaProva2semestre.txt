Escreva um programa que leia 3 notas de 5 alunos e a média das notas dos exercícios 
realizados por eles. Calcular a média de aproveitamento, usando a fórmula: MA = (N1 
+ N2*2 + N3*3 + ME)/7.
    double notas[5][5];
    for (int i = 0; i < 5; ++i)  -> linhas que representam 05 alunos
    printf("Dados do aluno: [%d] \n", i + 1);
    for (int j = 0; j < 4; ++j) 
   printf("Entre com a nota %d:  \n", j + 1);  scanf("%lf", &notas[i][j]);  }
   //MA = (N1 //+ N2*2 + N3*3 + ME)/7
     notas[i][4] = (notas[i][0] + notas[i][1] * 2 + notas[i][2] * 3 + notas[i][3]) / 7; }
    printf("Media de aproveitamento de cada aluno\n");
    for (int i = 0; i < 5; ++i) {
     printf("Media de aproveitamento do aluno %d ===> %.2lf\n", i+1, notas[i][4]);  }

Faça um programa que com uso da estrutura for. Determine se um número dado pelo 
usuário é primo, ou não.*/
    int numero;
    do {
        printf("Digite o numero a ser testado: \n");
        scanf("%d", &numero);   }while(numero< 2);
    int primo = 1;
    for (int i = 2; i < numero/2; ++i) {
        if(numero % i == 0){  primo = 0;
            break;
        }   }
primo ? printf("O numero eh primo \n") : printf("O numero nao eh primo \n");

3 Faça um programa que receba 10 dados do usuário e mostre a média dos valores 
entrados pelo usuário, use a estrutura while, para receber dez valores ou sair quando o 
usuário entrar com o valor 0.*/
    int cont = 0; int numero;  int soma = 0;
    do{
        printf("Digite um valor, ou 0 para sair: \n");  scanf("%d", &numero);
        soma += numero;
        if(numero != 0)cont++;   }while(cont < 10 && numero!=0);
    double  media = 0.0;  if(cont!=0){
        media = (double)soma / cont;
    }   printf("A media é: %.2lf \n", media);

Durante uma corrida de automóveis com N voltas (onde
0 < N < 15) de duração foram anotados, para um piloto,
na ordem, os tempos registrados em cada volta. fazer
 um programa em C para ler os tempos das N voltas.
 Calcular e imprimir:* a) melhor tempo; b) a volta em que ocorreu o melhor tempo;
 c) tempo médio das N voltas
    int nvoltas= 0 , melhorVolta= 0 ;
    tempo duplo , tempomedio= 0.0 , somaTempo= 0.0 , menorTempo= 0.0 ;
    do {
     printf ( " Digite o numero de voltas: " );scanf ( " %d " , &nvoltas);
    } while (nvoltas<= 0 || nvoltas>= 15 );
    for ( int i = 1 ; i <= nvoltas; ++i) {  printf ( " Digite o tempo da %d a) volta \n " ,i);
        scanf ( " %lf " , &tempo);   if (i== 1 ){
            menorTempo = tempo; melhorVolta = 1 ; }
        if (tempo < menorTempo){
            menorTempo = tempo;melhorVolta = i;
        }  somaTempo+= tempo;
    } tempomedio = somaTempo / nvoltas;
printf ( " Melhor volt em tempo: %lf , Melhor volta numerica: %d,
  Melhor volta numerica: %d  " , menorTempo, ,melhorVolta,    tempomedio);

Fazer um programa em C para calcular a somatória dos
N primeiros divisores de um inteiro X, onde N e X
são lidos e são números inteiros e positivos. [Validar entradas].
    int x, n;
    printf ( " Entre com o valor inteiro e positivo de x: \n " );  scanf ( " %d " , &x);
    do{
        printf ( " Digite o valor inteiro e positivo de n: \n " ); scanf ( " %d " , &n);
    } while (n<= 0 || n>x);
    int soma = 0 ;  int contdivisores = 0 ;
    for ( int i = 1 ; i <= x; ++i) {  if (x % i == 0 ) {
           soma+=i;contdivisores++; }
       if (contdivisores == n) break ; }
    printf ( " Somatoria eh: %d  \n " ,soma);
    printf ( " Quantidade de divisores considerados: %d  \n " , contdivisores);

Faça o programa que apresenta a seguinte saída,
acompanhando o usuário o número máximo (no exemplo, 9).
Este número deve ser sempre ímpar.
    int n;  do {
     printf ( " Digite um valor impar \n " ); scanf ( " %d " , &n);
    } while (n% 2 == 0 );
    for ( int i = 1 ; i <= n; i++) {  for ( int j = i; j <= n; j++) {
            printf ( " %d  " , j); }  printf ( " \n " );   }
irá imprimir por exemplo: linha de cima: 1 2 3 4 5, linha de baixo 2 3 4 5. Sucessivamente

Escreva um programa em C para ler 04 pares de valores inteiros e positivos, 
valide essa entrada. Para cada par lido deve ser impresso o valor do maior elemento do par
 ou a frase "Valores Iguais" quando o forem.
    int num1, num2;
    for ( int i = 1 ; i <= 4 ; i++) { // Estrutura para receber quatro pares de valores
     do{ printf ( " Entre com dois valores inteiros e positivos: \n " );
            scanf ( " %d%d " , &num1, &num2);
   } while (num1 <= 0 || num2<= 0 );
   if (num1 == num2){
   printf ( " Par de valores entrados eh igual \n " );
 } 
num1 > num2 ? printf ( " Primeiro numero eh maior: %d  \n " , num1) :
 printf ( " Segundo numero eh maior: %d  \n " , num2); }

4    Escreva um programa em C que leia 05 números inteiros positivos. 
Para cada número escreva a soma de seus divisores (exceto ele mesmo).
  int n, i, j, soma;
for (i = 0; i < 5; i++) { printf("Digite um número inteiro positivo: ");
        scanf("%d", &n);
 soma = 0;
        for (j = 1; j < n; j++) {
            if (n % j == 0) { soma += j;
            }
        }  printf("A soma dos divisores de %d é %d.\n", n, soma);

definir um vetor de 10 numeros inteiros que deve conter como dados, os 10 primeiros numeros primos.
  int primos[100] = {0};  int x = 2; //primo inicial
    int cont = 0; // contagem dos primos encontrados  do{ int eh_primo = 1;
        for(int i=2; i<=x/2 ; i++){   if(x % i ==0){    eh_primo = 0;
                break;      }  }   if(eh_primo) {
            primos[cont] = x; cont++;   }
        x++;
    }while(cont < 100)   for (int i = 0; i < 100; ++i) {
        printf("[%2d] ", primos[i]);  }
    printf("\nAcima numeros primos (100 primeiros)" );}

Nesse exemplo o numero 1 é imprimido de forma horizontal tombado, assim  \
    int tamanho;
    printf("Qual o tamanho da matriz (linhas) \n"); scanf("%d", &tamanho);
    int matriz[tamanho][tamanho];//algoritmo para gerar e apresentar uma matriz identidade
    for (int i = 0; i < tamanho; ++i) { for (int j = 0; j < tamanho; ++j) {
            matriz[i][j] = i==j ? 1 : 0;      printf("[%2d] ", matriz[i][j]);      } printf("\n");

Nesse exemplo uma matriz é gerada com valores aleatórios.
#include <stdlib.h> #include <time.h> srand(time(NULL));
    int matriz[4][4]; //algoritmo para preencher a matriz com valores de 0 a 9
    for (int i = 0; i < 4; ++i) {
        for (int j = 0; j < 4; ++j) {
            matriz[i][j] = rand() % 10; }   }
    //para apresentar os dados (percorrer) for (int i = 0; i < 4; ++i) {  for (int j = 0; j < 4; ++j) {
            printf("[%2d] ", matriz[i][j]);   }    printf("\n");  }

Nesse exemplo são gerados valores aleatórios apenas na parte triangular inferior da matriz
#include <stdlib.h> #include <time.h> #define T 7
    int matriz[T][T] = {0};
    for (int i = 0; i < T; ++i) {     for (int j = 0; j <= i; ++j) { <- Nessa parte, se J receber i, serão gerados números apenas na horizontal tombada. Se na 2º parte j < i, os zeros serão imprimidos na primeira linha tbm. Para imprimir a matriz com valores aleatórios na parte triangular superior é só trocar o i por j e o j por i nos 2 for’s.
            matriz[i][j] = (rand() % 9) + 1;   }  }
   //apresentar a matriz     for (int i = 0; i < T; ++i) {       for (int j = 0; j < T; ++j) {
            printf("[%2d] ", matriz[i][j]); }        printf("\n");

Desenvolva um programa que faça a leitura de 10 valores no vetor A. Construir um vetor B do mesmo tipo, observando a seguinte formatação: Se o valor do índice for par, o valor deverá ser multiplicado por 5;
Se o valor do índice for ímpar, deverá ser somado com 5. Ao final mostrar os conteúdos dos dois vetores invertidos (listar ao contrário

int vetor_a[10] = {0};        int vetor_b[10] = {0};     //entrada de dados (10 valores) ->  for (int i = 0; i < 10; ++i) {
        printf("Digite um valor: \n");  scanf("%d", &vetor_a[i]);   }
    //logica do exercício     for (int i = 0; i < 10; ++i) {
        vetor_b[i] = i % 2 ==0 ? vetor_a[i] * 5 : vetor_a[i] + 5;     }
    //apresentar o vetor_a      for (int i = 0; i < 10; ++i) {   printf("[%3d] ", vetor_a[i]);    }    printf("\n");
    //apresentar o vetor_b      for (int i = 0; i < 10; ++i) {   printf("[%3d] ", vetor_b[i]);

Escreva um programa em linguagem C que declare um vetor com n=10 números reais e coloque na i-ésima posição o resultado de i*(n-i)
  int n = 10;  float vetor[n];      for (int i = 0; i < n; i++) {    vetor[i] = i * (n-i);   }    printf("Vetor resultante:\n");
  for (int i = 0; i < n; i++) {    printf("%f ", vetor[i]);    }        printf("\n"); 

Desenvolva um programa em C que leia 5 elementos de um vetor A.  No final, apresente:
• A soma de todos os valores ímpares. • A soma de todos os valores pares. • A soma total. • E a porcentagem de números ímpares em relação aos pares.
  int vetor[5], i;  int soma_impares = 0, soma_pares = 0, soma_total = 0;   int num_impares = 0, num_pares = 0;
  float porcentagem_impares;
  printf("Digite os 5 elementos do vetor:\n");     for (i = 0; i < 5; i++) {     scanf("%d", &vetor[i]);
    if (vetor[i] % 2 == 0) {   soma_pares += vetor[i];   num_pares++;
    } else {     soma_impares += vetor[i];     num_impares++;    }
    soma_total += vetor[i];   }
 printf("\nSoma dos valores ímpares: %d\n", soma_impares);    printf("Soma dos valores pares: %d\n", soma_pares);       printf("Soma total: %d\n", soma_total);
if (num_pares == 0) {     porcentagem_impares = 100;      } else {     porcentagem_impares = (float)num_impares / num_pares * 100;     }
  printf("Porcentagem de números ímpares em relação aos pares: %.2f%%\n", porcentagem_impares);

Crie um programa em C que leia 8 valores em um vetor A. – Construir um vetor B com a mesma dimensão. Os
elementos do vetor A devem ser multiplicados por 3 e armazenado o resultado no vetor B. Ou seja, – B[1] = A[1] * 3; por exemplo.
   int A[8], B[8];     int i;
 // Lê os valores do vetor A   for(i=0; i<8; i++) {     printf("Digite o valor de A[%d]: ", i);     scanf("%d", &A[i]);   }
 // Multiplica os valores do vetor A por 3 e armazena no vetor B      for(i=0; i<8; i++) {      B[i] = A[i] * 3;     }
 // Imprime os valores do vetor B     printf("\nVetor B:\n");     for(i=0; i<8; i++) {     printf("B[%d] = %d\n", i, B[i]);     }

Crie em C um vetor A com 5 posições. – O usuário deverá fornecer o valor para cada campo, ao final será mostrado como resultado este mesmo vetor A, porém em ordem crescente de valores.
int i, j, temp, vetor[5];
  // Solicita ao usuário que insira um valor para cada posição do vetor
   for (i = 0; i < 5; i++) {     printf("Insira um valor para a posição %d do vetor: ", i);    scanf("%d", &vetor[i]);   }
// Ordena o vetor em ordem crescente
   for (i = 0; i < 5; i++) {         for (j = i+1; j < 5; j++) {       if (vetor[i] > vetor[j]) {     temp = vetor[i];                                         vetor[i] = vetor[j];     vetor[j] = temp;   }     }     }
// Exibe o vetor ordenado na tela      printf("\nVetor ordenado em ordem crescente: ");    for (i = 0; i < 5; i++) {
       printf("%d ", vetor[i]); }

Desenvolver um em C programa que efetue a leitura de 8 RAs de alunos e também suas duas notas bimestrais.
– Ao final o programa deverá exibir o RA do aluno bem como sua média final.
 int ra[8], nota1[8], nota2[8];   float media[8];
    // Lendo os dados dos alunos   for (int i = 0; i < 8; i++) {
        printf("Digite o RA do aluno %d: ", i+1);         scanf("%d", &ra[i]);
        printf("Digite a nota do primeiro bimestre do aluno %d: ", i+1);      scanf("%d", &nota1[i]);
        printf("Digite a nota do segundo bimestre do aluno %d: ", i+1);       scanf("%d", &nota2[i]);
  // Calculando a média do aluno
        media[i] = (nota1[i] + nota2[i]) / 2.0;
        printf("\n");
    }
    // Exibindo as médias dos alunos
    printf("Médias finais dos alunos:\n");
    for (int i = 0; i < 8; i++) {
        printf("RA: %d | Média: %.2f\n", ra[i], media[i]);
    }

Faça um programa em C que leia duas matrizes A e B, cada uma com uma dimensão de 4 linhas por duas colunas.
– Construa uma matriz C com a mesma dimensão que seus elementos deverão conter as somas dos valores de mesma posição na matriz A e B. – Ex: – MatrizC[0][1] = MatrizA[0][1] + MatrizB[0][1]
#define LINHAS 4
#define COLUNAS 2
    int matrizA[LINHAS][COLUNAS];  int matrizB[LINHAS][COLUNAS];   int matrizC[LINHAS][COLUNAS];   int i, j;
 // Leitura da matriz A
    printf("Matriz A\n");       for (i = 0; i < LINHAS; i++) {       for (j = 0; j < COLUNAS; j++) {
            printf("Digite o elemento A[%d][%d]: ", i, j);       scanf("%d", &matrizA[i][j]);    }    }
  // Leitura da matriz B
    printf("\nMatriz B\n");      for (i = 0; i < LINHAS; i++) {      for (j = 0; j < COLUNAS; j++) {
            printf("Digite o elemento B[%d][%d]: ", i, j);     scanf("%d", &matrizB[i][j]);      }      }
  // Construção da matriz C     for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {      matrizC[i][j] = matrizA[i][j] + matrizB[i][j];    }   }
   // Impressão da matriz C
    printf("\nMatriz C (A + B)\n");      for (i = 0; i < LINHAS; i++) {      for (j = 0; j < COLUNAS; j++) {
            printf("%d ", matrizC[i][j]);       }         printf("\n");     }

Escreva um algoritmo em  linguagem C que gere uma PA de razão qualquer, com uma série de 10 termos iniciando em 1.
    int a1 = 1; // primeiro termo da PA    int r; // razão da PA   int i; // contador do loop
 printf("Digite a razão da PA: ");    scanf("%d", &r);
  printf("Série de 10 termos da PA com razão %d e primeiro termo %d:\n", r, a1);
    printf("%d ", a1);
for(i = 1; i < 10; i++) {       int termo = a1 + i * r;     printf("%d ", termo);   }

Faça um programa em C que leia X números N onde (0<=N<20). Ao final, apresente a somatória dos mesmos. A 
condição de parada é a entrada de um valor 0.
int n; // número fornecido pelo usuário     int soma = 0; // variável que armazena a somatória dos números
  do {     printf("Digite um número entre 0 e 19 (0 para encerrar): ");      scanf("%d", &n);
  if(n >= 0 && n < 20) {     soma += n;  }       else if(n != 0) {     printf("Número inválido!\n");    }
    } while(n != 0);        printf("A somatória dos números digitados é: %d\n", soma);

Faça um programa em C que dados 10 números pelo usuário, verifique quantos são pares.
int num, count = 0;
      printf("Digite 10 numeros:\n");    for (int i = 0; i < 10; i++) {      scanf("%d", &num);
        if (num % 2 == 0) {      count++;   }     }      printf("Existem %d numeros pares.\n", count);

Construa um programa em C que leia 5 valores inteiros e: Encontre o maior valor, o menor valor e calcule a média dos números lidos.
int num, max, min, sum = 0;   float avg;
     // leitura do primeiro número para inicializar as variáveis
    printf("Digite um numero: ");
    scanf("%d", &num);     max = num;     min = num;    sum += num;
     // leitura dos próximos 4 números    for (int i = 0; i < 4; i++) {
        printf("Digite mais um numero: ");       scanf("%d", &num);
         // verifica se o número é maior que o atual máximo    if (num > max) {
            max = num;   }
           // verifica se o número é menor que o atual mínimo    if (num < min) {
            min = num; } 
        // soma o número ao acumulador para calcular a média    sum += num; }
    // calcula a média dos números lidos    avg = (float) sum / 5; 
    // exibe os resultados
    printf("O maior valor digitado foi: %d\n", max);
    printf("O menor valor digitado foi: %d\n", min);
    printf("A media dos numeros digitados foi: %.2f\n", avg);

Desenvolver um programa em C que leia 5 elementos de um vetor A. – No final, apresente: a. A soma de todos os valores ímpares. b. A soma de todos os valores pares.  c. A soma total.  d. E a porcentagem de números ímpares e de pares.
int A[5], soma_impar = 0, soma_par = 0, soma_total = 0, num_impares = 0, num_pares = 0;
    float porc_impares, porc_pares;
  // Lendo os 5 elementos do vetor A
    printf("Digite os 5 elementos do vetor A:\n");
    for (int i = 0; i < 5; i++) {
        scanf("%d", &A[i]);
        soma_total += A[i];
        if (A[i] % 2 == 0) {
            soma_par += A[i];
            num_pares++;
        } else {
            soma_impar += A[i];
            num_impares++;
        }    }
    // Calculando a porcentagem de números ímpares e pares
    porc_impares = (float) num_impares / 5 * 100;
    porc_pares = (float) num_pares / 5 * 100;
// Exibindo os resultados
    printf("\nSoma dos valores ímpares: %d\n", soma_impar);
    printf("Soma dos valores pares: %d\n", soma_par);
    printf("Soma total: %d\n", soma_total);
    printf("Porcentagem de números ímpares: %.2f%%\n", porc_impares);
    printf("Porcentagem de números pares: %.2f%%\n", porc_pares);

Desenvolva um programa em C que faça a leitura de 10 valores no vetor A. Construir um vetor B do mesmo tipo, observando a seguinte formatação: a. Se o valor do índice for par, o valor deverá ser multiplicado por 5; b. Se o valor do índice for ímpar, deverá ser somado com 5. c. Ao final mostrar os conteúdos dos dois vetores invertidos (listar ao contrário).
int A[10], B[10];  int i;
  // Leitura dos valores do vetor A     for(i=0; i<10; i++)
    {     printf("Digite o valor de A[%d]: ", i);     scanf("%d", &A[i]);    }
  // Construção do vetor B com as formatações solicitadas  for(i=0; i<10; i++)
    {     if(i % 2 == 0)  // índice par
        {     B[i] = A[i] * 5;     }
        else  // índice ímpar
        {    B[i] = A[i] + 5;    }
    }
 // Impressão dos vetores invertidos
    printf("\nVetor B: ");
    for(i=9; i>=0; i--)
    {
        printf("%d ", B[i]);    }
      
  printf("\nVetor A: ");
    for(i=9; i>=0; i--)
    {
        printf("%d ", A[i]);      }


Crie um programa em C Crie um programa que lê 10 valores inteiros e, em seguida, mostre na tela os valores 
lidos na ordem inversa.
int valores[10];
   printf("Digite 10 valores inteiros:\n");
// leitura dos valores
  for(int i = 0; i < 10; i++) {       scanf("%d", &valores[i]);   }
printf("Valores lidos na ordem inversa:\n");
// exibição dos valores na ordem inversa
  for(int i = 9; i >= 0; i--) {
    printf("%d ", valores[i]);    }

Crie um programa que lê 10 valores inteiros pares e, em seguida, mostre na tela os
valores lidos na ordem inversa. 
int numeros[10];    int i;
 // Loop para ler 10 valores inteiros pares
    for (i = 0; i < 10; i++) {
        do {      printf("Digite o %dº número par: ", i+1);     scanf("%d", &numeros[i]);
        } while (numeros[i] % 2 != 0);   }
// Imprime os valores lidos na ordem inversa
    printf("Valores lidos na ordem inversa:\n");
    for (i = 9; i >= 0; i--) {      printf("%d\n", numeros[i]);   }

Faça um programa para ler a nota da prova de 15 alunos e armazene num vetor, 
calcule e imprima a média geral. 
#define NUM_ALUNOS 15
int main() {
    float notas[NUM_ALUNOS];    float media = 0;
 // Lê as notas dos alunos e armazena no vetor
    for (int i = 0; i < NUM_ALUNOS; i++) {
        printf("Digite a nota do aluno %d: ", i+1);
        scanf("%f", &notas[i]);
  // Soma a nota à média geral
        media += notas[i];     }
  // Calcula a média geral
    media /= NUM_ALUNOS;
  // Imprime a média geral
    printf("A media geral da turma foi %.2f\n", media); ]

4   int vetor[5];  int  i, j, soma;
 // Lê 5 números inteiros positivos para o vetor
    for (i = 0; i < 5; i++) {      printf("Digite um número inteiro positivo: ");       scanf("%d", &vetor[i]);   }
// Calcula a soma dos divisores de cada número
    for (i = 0; i < 5; i++) {      soma = 0;
        for (j = 1; j < vetor[i]; j++) {       if (vetor[i] % j == 0) {
                soma += j;      }  }       printf("A soma dos divisores de %d é %d\n", vetor[i], soma);  }


3int valores[10], i = 0, soma = 0;    float media;       printf("Digite os valores (ou 0 para sair):\n");
  while (i < 10) {         scanf("%d", &valores[i]);        if (valores[i] == 0) {       break;  }
   soma += valores[i];         i++;       }
 media = soma / (float)i;      printf("Média dos valores entrados: %.2f\n", media);

mesmo exercico, forma diferente.
  int i, n = 0;     double soma = 0, media;     double vetor[MAX];      printf("Entre com os valores (digite 0 para sair):\n");
     // lê os valores e armazena no vetor      for (i = 0; i < MAX; i++) {      scanf("%lf", &vetor[i]);
           if (vetor[i] == 0) {      // se o valor digitado for 0, sai do loop
            n = i; // define a quantidade de elementos válidos no vetor
            break;      }       soma += vetor[i]; // acumula a soma dos valores    }
       if (n > 0) { // se há elementos válidos no vetor
        media = soma / n;      // calcula a média       printf("Média: %.2lf\n", media);
    } else { // caso contrário, avisa que nenhum valor foi digitado      printf("Nenhum valor digitado.\n");  }

Faça um programa em C que leia 10 números em um vetor e mostre quais são primos e quantos são.
int vetor[10], primos = 0;      printf("Digite 10 valores:\n");
      // Lê os valores do vetor    for (int i = 0; i < 10; i++) {    scanf("%d", &vetor[i]);    }
     // Verifica quais valores são primos e incrementa a variável primos    for (int i = 0; i < 10; i++) {
        int primo = 1; // assume que o número é primo
          if (vetor[i] < 2) {     primo = 0; // números menores que 2 não são primos      }
        else {     for (int j = 2; j < vetor[i]; j++) {      if (vetor[i] % j == 0) {
                    primo = 0; // se o número é divisível por algum outro, não é primo        break; } } }
             if (primo == 1) {       printf("%d eh primo.\n", vetor[i]);      primos++;  }  }
    // Mostra a quantidade de valores primos       printf("\n%d valores sao primos.\n", primos);

Faça um programa em C que leia 10 números em um vetor e mostre quantos são primos e faça a soma somente dos números primos
int vetor[10], i, j, primo, somaPrimos = 0, contPrimos = 0;
// Lê os 10 números e armazena no vetor     for (i = 0; i < 10; i++) {     printf("Digite um número: ");
    scanf("%d", &vetor[i]);   }
// Verifica quais números do vetor são primos e faz a soma      for (i = 0; i < 10; i++) {       primo = 1;
 // Verifica se o número é primo      for (j = 2; j < vetor[i]; j++) {
      if (vetor[i] % j == 0) {
        primo = 0;      break;  } }
    if (primo == 1 && vetor[i] > 1) {
      somaPrimos += vetor[i];
      contPrimos++; } }     printf("Quantidade de números primos: %d\n", contPrimos);    printf("Soma dos números primos: %d\n", somaPrimos);







    }        
