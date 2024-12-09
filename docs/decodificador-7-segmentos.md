# Decodificador de 7 segmentos (Hexadecimal)

## 🔍 Descrição

Este circuito decodifica valores binários de 4 bits em padrões para um display de 7 segmentos, exibindo números e caracteres hexadecimais:

- Números de 0 a 9.
- Letras de A a F.

Para entradas maiores que 15 (1111), o comportamento é considerado inválido e pode exibir padrões arbitrários.

## 🖥️ Componentes

**Os principais componentes usados no circuito incluem:**
   - **Portas Lógicas**: AND, OR, NOT.
   - **Entradas**:
     - \( A[3:0] \): Entrada binária de 4 bits.
   - **Saídas**:
     - \( a, b, c, d, e, f, g \): Sinais que controlam os segmentos do display.
    
![Screenshot 2024-12-09 190311](https://github.com/user-attachments/assets/ee3b6cc9-ad80-46d7-8a7a-4e2cb3dbcb86)

## ⚙️ Implementação

1. **Descrição do Circuito**:

   - Ultilizando as portas lógicas (AND,OR E NOT) e a lógica apresentada na imagem construimos o circuito verificando cada caso e principalmente ultilizando a porta not  para bloquear algumas passagens.

2. **Imagem/video do Circuito**:

   https://github.com/user-attachments/assets/9c2b1212-421f-4083-8309-4247799994a7

   ---
   ![Screenshot 2024-12-09 190933](https://github.com/user-attachments/assets/10180b2d-4b84-4d85-970f-e9ba10a139e2)

   ---
   ![Screenshot 2024-12-09 190941](https://github.com/user-attachments/assets/748bd4f9-1e0f-450b-8f24-2e903d66a50f)

   

## 🔬 Testes

1. **Método de Teste**:

   - Apesar dos muitos casos e assim gerando difculdade pra fazer o circuito. Ele apresentou exatidão no resultado
   

2. **Resultados dos Testes**:
   ## Tabela Verdade do Decodificador de 7 Segmentos

   A tabela a seguir mostra as entradas e as ativações dos segmentos (\( a, b, c, d, e, f, g \)) para exibir números e letras hexadecimais no display de 7 segmentos.
   
   | Entrada (\( A[3:0] \)) | \( a \) | \( b \) | \( c \) | \( d \) | \( e \) | \( f \) | \( g \) | Caracter Exibido |
   |-------------------------|---------|---------|---------|---------|---------|---------|---------|------------------|
   | 0000 (0)               |   1     |   1     |   1     |   1     |   1     |   1     |   0     | 0                |
   | 0001 (1)               |   0     |   1     |   1     |   0     |   0     |   0     |   0     | 1                |
   | 0010 (2)               |   1     |   1     |   0     |   1     |   1     |   0     |   1     | 2                |
   | 0011 (3)               |   1     |   1     |   1     |   1     |   0     |   0     |   1     | 3                |
   | 0100 (4)               |   0     |   1     |   1     |   0     |   0     |   1     |   1     | 4                |
   | 0101 (5)               |   1     |   0     |   1     |   1     |   0     |   1     |   1     | 5                |
   | 0110 (6)               |   1     |   0     |   1     |   1     |   1     |   1     |   1     | 6                |
   | 0111 (7)               |   1     |   1     |   1     |   0     |   0     |   0     |   0     | 7                |
   | 1000 (8)               |   1     |   1     |   1     |   1     |   1     |   1     |   1     | 8                |
   | 1001 (9)               |   1     |   1     |   1     |   1     |   0     |   1     |   1     | 9                |
   | 1010 (A)               |   1     |   1     |   1     |   0     |   1     |   1     |   1     | A                |
   | 1011 (B)               |   0     |   0     |   1     |   1     |   1     |   1     |   1     | B                |
   | 1100 (C)               |   1     |   0     |   0     |   1     |   1     |   1     |   0     | C                |
   | 1101 (D)               |   0     |   1     |   1     |   1     |   1     |   0     |   1     | D                |
   | 1110 (E)               |   1     |   0     |   0     |   1     |   1     |   1     |   1     | E                |
   | 1111 (F)               |   1     |   0     |   0     |   0     |   1     |   1     |   1     | F                |

---

## 📈 Análise

Resultado foi como esperado, a lógica da imagem onde vemos as entradas que ativam determinados leds facilitaram a checagem 

## 📂 Arquivos Relacionados

- [Arquivo do Logisim](../src/nome-do-arquivo.circ)
