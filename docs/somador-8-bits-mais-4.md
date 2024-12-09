# Somador 8 bits (inteiro + 4)

## 🔍 Descrição

Circuito combinacional utilizado para somar dois números um inteiro e 4 (100 em binário) , gerando uma soma e, opcionalmente, um bit de transporte de saída (carry-out).

## 🖥️ Componentes

- **Pin (inteiro)**

   - Ultilização de pin que tem como valor números inteiros e passa binário além de pinos para a saida de resultados, assim como carry out e carry in 
   
- **Portas lógicas**

   - Ultilização de portas NAD,XOR E OR para conseguirmos o resultado esperado
   
- **Componentes menores**

   - ultilização de somadores de menos bit para a implementação do de 8 bits
- **constante**

   - Ultilizamos uma constante para sempre somar mais quatro

## ⚙️ Implementação

1. **Descrição do Circuito**:

- Com a ultilização de portas lógicas podemos cobrir as possibilidade de soma de número binário, que são:
     
     |Possiblidades|Resultados|
     |-------------|----------|
     |0+0|0|
     |1+0|1|
     |1+1|0|

   - Lembrando da existência do carry out, que pegará o que passou por conta da soma  1+1 (1+1=0 e passa 1)
 
   - Para enteder a soma de 8 bits vamos ver primeiro a soma de 1 bit, o circuito é dividido e duas partes. A primeira responsável por fazer a soma, já a segunda responsável pelo carry out, ou    seja o bit que    
   vai passar pra próxima soma. Lembrando que temos o cin ou carry in que seria o 1 que foi passado chegando nessa soma, mas como é apenas soma de um bit
   ele só será necessário pra quando aprimorarmos o circuito, a gente ter acesso a ele, caso contrário podemos apenas aterrar.

   ![Screenshot 2024-12-09 155440](https://github.com/user-attachments/assets/469bd7f1-ce93-4bf0-a754-3bc4483ee2b8)

2. **Imagem do Circuito**:

   ![Screenshot 2024-12-09 181542](https://github.com/user-attachments/assets/a5c16d3a-ea15-4d41-ae3d-972073474fc0)

   Seguindo a lógica do circuito somador, proposto aqui mesmo nesse repositório:
   
   - [Arquivo do Logisim Evolution](../src/somador-8-bits.circ)

     Onde temos a ultilização de portas XOR para calcular soma de bits, além do carry out e carry in para passagem de soma estourada, uma mudança para o somador normal é que no somador de 4 bits da direita, temos ele automaticamente somando os bits do input com quatro, ultilizando constantes.

   - Somador 4 bits direita

     ![Screenshot 2024-12-09 182526](https://github.com/user-attachments/assets/32b94249-047d-4811-a349-f35875658224)

   - Somador 4 bits esquerda
  
     ![Screenshot 2024-12-09 182057](https://github.com/user-attachments/assets/26eaa1a6-8199-428e-be11-55812cce36e5)

   
   

## 🔬 Testes

1. **Método de Teste**:

   https://github.com/user-attachments/assets/1e175f37-4580-4d69-b392-ca04347059e3

2. **Resultados dos Testes**:
   - Como tabela verdade de 8bits ou seja suas somas são muitas trouxemos a a soma de 4 bits pra exemplificar:

     | Entrada (binária) | Soma Fixa (+4) | Saída (S[3:0]) | Carry-out (Cout) |
      |-------------------|----------------|----------------|------------------|
      | 0000             | 0100          | 0100           | 0                |
      | 0001             | 0100          | 0101           | 0                |
      | 0010             | 0100          | 0110           | 0                |
      | 0011             | 0100          | 0111           | 0                |
      | 0100             | 0100          | 1000           | 0                |
      | 0101             | 0100          | 1001           | 0                |
      | 0110             | 0100          | 1010           | 0                |
      | 0111             | 0100          | 1011           | 0                |
      | 1000             | 0100          | 1100           | 0                |
      | 1001             | 0100          | 1101           | 0                |
      | 1010             | 0100          | 1110           | 0                |
      | 1011             | 0100          | 1111           | 0                |
      | 1100             | 0100          | 0000           | 1                |
      | 1101             | 0100          | 0001           | 1                |
      | 1110             | 0100          | 0010           | 1                |
      | 1111             | 0100          | 0011           | 1                |

## 📈 Análise

Os resultados estão alinhados com o esperado, baseando-se na lógica projetada.

- Exemplo de comportamento esperado:
   input= 14 (1100) + 0100 = 10010 (18 decimal)

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](../src/Somador8bitsplus4.circ)
