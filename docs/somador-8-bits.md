# Somador 8 bits

## 🔍 Descrição

circuito combinacional utilizado para somar dois números binários de 8 bits, gerando uma soma e, opcionalmente, um bit de transporte de saída (carry-out).

## 🖥️ Componentes

- **Pins**

   - Ultilização de pins para entrada do número binário e saida de resultados, assim como carry out e carry in 
   
- **Portas lógicas**

   - Ultilização de portas NAD,XOR E OR para conseguirmos o resultado esperado
   
- **Componentes menores**

   - ultilização de somadores de menos bit para a implementação do de 8 bits

## ⚙️ Implementação

1. **Descrição do Circuito**:

   - Com a ultilização de portas lógicas podemos cobrir as possibilidade de soma de número binário, que são:
     
     |Possiblidades|Resultados|
     |-------------|----------|
     |0+0|0|
     |1+0|1|
     |1+1|0|

   - Lembrando da existência do carry out, que pegará o que passou por conta da soma  1+1 (1+1=0 e passa 1)


2. **Imagem do Circuito**:

   - **Como nosso circuito é formado por circuitos menores vamos por parte**
   
    ![Screenshot 2024-12-09 155440](https://github.com/user-attachments/assets/469bd7f1-ce93-4bf0-a754-3bc4483ee2b8)

   **Somador bit a bit**: Para enteder a soma de 8 bits vamos ver primeiro a soma de 1 bit< o circuito é dividido e duas partes. A primeira responsável por fazer a soma, já a segunda responsável pelo carry out, ou    seja o bit que vai passar pra próxima soma. Lembrando que temos o cin ou carry in que seria o 1 que foi passado chegando nessa soma, mas como é apenas soma de um bit
   ele só será necessário pra quando aprimorarmos o circuito, a gente ter acesso a ele, caso contrário podemos apenas aterrar.
   
    ![Screenshot 2024-12-09 155447](https://github.com/user-attachments/assets/3ff0f315-3aaf-4f82-ab9b-c6b55240df9a)

   **Somador 4 bit**: Funciona exatamente como o primeiro somamos um bit de cada vez da direita pra esquerda, e dssa vez ligamos o carry out ao carry do próximo, dessa forma se chegarmos a algum caso de passagem, pois extrapolou a soma, o bit passará para próxima soma.
    
    ![Screenshot 2024-12-09 155455](https://github.com/user-attachments/assets/b44bb412-d2fc-4e18-b9f4-1ea6b64f3370)

   **Somador 4 bit**: Não existe nenhum segredo, funcionamento igual ao de 4 bits, e com isso percebemos que podemos criar somadores de 16, 32 e por aí vai, apenas seguindo essa lógica simples> a soma ocorre bita bit e qunado o ocorre carry out passamos para próxima soma e ultilizamos o carry out e carry in pra juntar os somadores quando chegamos no somador de nossa preferência~, podemos aterra o carry in mais a direita, já que na primeira soma não temos passagem de uma soma anterior. 

## 🔬 Testes

1. **Método de Teste**:

   - O principal ponto é a solução de somas binárias específicas e a criação de um circuito que respeite os resultados corretos e atue corretamente.
   - Pelo tamanho de possiblidades que uma tabela do somador 8 bits tem, decidimos colcoar a de 1 bit, e assim mostrar um pouco do funcionamento.
     
     
      | A | B | Cin | S | Cout |
      |---|---|-----|---|------|
      | 0 | 0 |  0  | 0 |  0   |
      | 0 | 0 |  1  | 1 |  0   |
      | 0 | 1 |  0  | 1 |  0   |
      | 0 | 1 |  1  | 0 |  1   |
      | 1 | 0 |  0  | 1 |  0   |
      | 1 | 0 |  1  | 0 |  1   |
      | 1 | 1 |  0  | 0 |  1   |
      | 1 | 1 |  1  | 1 |  1   |

   
3. **Resultados dos Testes**:
   
   https://github.com/user-attachments/assets/f97ef253-7cb9-4480-9514-a57651a4797a

## 📈 Análise

Especialmente pela soma de um bit conseguimos montar um circuito que pode somar 8, e com grande ajuda do carry out e carry in que possiblita essa junção de somas.

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](../src/somador-8-bits.circ)
