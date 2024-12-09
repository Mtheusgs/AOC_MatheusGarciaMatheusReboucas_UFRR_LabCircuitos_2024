# ULA (Unidade Lógica e Aritmética)

## 🔍 Descrição

A ULA (Unidade Lógica e Aritmética) é um componente fundamental em processadores, responsável por realizar operações lógicas (e.g., AND, OR, XOR) e aritméticas (e.g., soma, subtração). Este projeto implementa uma ULA com suporte a múltiplas operações, controladas por sinais de entrada específicos.

O objetivo é projetar um circuito que seja capaz de executar operações básicas em dois operandos (\( A \) e \( B \)) e produzir o resultado adequado, com suporte a sinalizações como carry-out, overflow e zero.

---

## 🖥️ Componentes

Os principais componentes utilizados no circuito incluem:
- **Portas Lógicas**: AND, OR, XOR, NOT.
- **Somador/Subtrator**: Circuito para operações de soma e subtração.
- **Multiplexadores**: Para selecionar a operação com base no sinal de controle.
- **Flip-Flops**: Caso seja necessário armazenar resultados (opcional).
- **Entradas**:
  -  Operandos de 8 bits.
  - \Seletor/Decoder/: Para selecionar a operação.
- **Saídas**:
  - pino de saida 8 bits: Resultado da operação.
  - \( Cout \): Carry-out (transporte).

---

## ⚙️ Implementação

### 1. **Descrição do Circuito**

   
### 2. **Imagem do Circuito**

   

---

## 🔬 Testes

### 1. **Método de Teste**

   - Para cada operação, foram testadas combinações diferentes de \( A \) e \( B \).
   - O circuito foi simulado no Logisim Evolution e os resultados foram comparados com valores esperados.

### 2. **Resultados dos Testes**


## Tabela de Operações e Testes

A tabela a seguir apresenta os testes realizados para uma ULA de 8 bits, com as operações na seguinte ordem:
1. AND (\( A \& B \))
2. OR (\( A | B \))
3. NOT (\( \sim A \))
4. NOT (\( \sim B \))
5. NAND (\( \sim(A \& B) \))
6. XOR (\( A \oplus B \))
7. Shift Left (\( A << 1 \))
8. Shift Right (\( A >> 1 \))
9. Soma (\( A + B \))
10. Subtração (\( A - B \))


| \( Op[3:0] \) | Operação              | Entrada (\( A \), \( B \))      | Saída (\( R[7:0] \)) | \( Cout \) | \( Z \) | \( OVF \) |
|---------------|-----------------------|---------------------------------|----------------------|------------|----------|-----------|
| 0000          | AND (\( A \& B \))   | 11001100, 10101010             | 10001000            | -          | 0        | -         |
| 0001          | OR (\( A | B \))     | 11001100, 10101010             | 11101110            | -          | 0        | -         |
| 0010          | NOT (\( \sim A \))   | 11001100, --------             | 00110011            | -          | 0        | -         |
| 0011          | NOT (\( \sim B \))   | --------, 10101010             | 01010101            | -          | 0        | -         |
| 0100          | NAND (\( \sim(A \& B) \)) | 11001100, 10101010         | 01110111            | -          | 0        | -         |
| 0101          | XOR (\( A \oplus B \)) | 11001100, 10101010           | 01100110            | -          | 0        | -         |
| 0110          | Shift Left (\( A << 1 \)) | 11001100, --------         | 10011000            | -          | 0        | -         |
| 0111          | Shift Right (\( A >> 1 \)) | 11001100, --------        | 01100110            | -          | 0        | -         |
| 1000          | Soma (\( A + B \))   | 11001100, 10101010             | 01110110            | 1          | 0        | 0         |
| 1001          | Subtração (\( A - B \)) | 11001100, 10101010          | 00000010            | 0          | 0        | 0         |

---

## Explicação da Tabela

- **Entradas (\( A, B \))**:
  - \( A = 11001100 \) (204 decimal)
  - \( B = 10101010 \) (170 decimal)
- **Operações**:
  - Operações lógicas (\( AND, OR, NOT, NAND, XOR \)) manipulam os bits diretamente.
  - Operações de deslocamento (\( << \), \( >> \)) ajustam os bits do operando \( A \).
  - Operações aritméticas (\( +, - \)) respeitam transporte (\( Cout \)) e estouro (\( OVF \)).
- **Saídas**:
  - \( R[7:0] \): Resultado da operação.
  - \( Cout \): Carry-out para soma/subtração.
  - \( Z \): Indicador de zero (1 se \( R = 0 \)).
  - \( OVF \): Indicador de overflow (para soma/subtração com sinal).


## 📈 Análise

### Resultados Obtidos

- A ULA funcionou corretamente para todas as operações descritas.

### Observações

1. **Complexidade**:
   - O circuito pode ser otimizado com o uso de multiplexadores mais eficientes para selecionar operações.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](../src/ULA.circ)
