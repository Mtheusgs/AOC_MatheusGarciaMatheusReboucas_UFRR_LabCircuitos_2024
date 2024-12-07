# Extensor de Sinal (4 bits para 8 bits)

## 🔍 Descrição

O Extensor de Sinal é um componente que expande um número de 4 bits para 8 bits, preservando o sinal (MSB - Most Significant Bit/Bit Mais Significativo). Este comportamento é essencial para garantir a correta representação de números binários assinados em complemento de 2.

---

## 🖥️ Componentes

- **Splitter(Distribuidor)**:
  - Recebe os 4 bits de entrada.
  - Replica o MSB para preencher os 4 bits mais significativos da saída.
- **Barramentos**:
  - Entrada: 4 bits.
  - Saída: 8 bits (4 bits menos significativos replicam os dados de entrada; 4 bits mais significativos replicam o MSB).

---

## ⚙️ Implementação

1. **Descrição do Circuito**:

   - **Entradas**:
     - Barramento de 4 bits: representa o valor inicial a ser expandido.
   - **Saídas**:
     - Barramento de 8 bits:
       - Os 4 bits menos significativos (`LSBs`) correspondem diretamente aos bits de entrada.
       - Os 4 bits mais significativos (`MSBs`) são preenchidos com o valor do MSB de entrada.
   - **Lógica**:
     - O MSB de entrada é replicado nos 4 bits mais significativos da saída.
     - Os bits de entrada são copiados diretamente para os LSBs da saída.

2. **Imagem do Circuito**:
   ![Extensor de Sinal](images/extensor_sinal_4_to_8.png)

---

## 🔬 Testes

1. **Método de Teste**:

   - Foram utilizados valores de entrada binários representando números positivos e negativos (complemento de 2).
   - A simulação foi realizada no Logisim Evolution, observando os valores de saída no barramento de 8 bits.

2. **Resultados dos Testes**:
   - **Tabela Verdade**:
     | Entrada (4 bits) | MSB | Saída (8 bits) |
     |------------------|-----|-------------------|
     | `0000` | 0 | `00000000` |
     | `0001` | 0 | `00000001` |
     | `0010` | 0 | `00000010` |
     | `0011` | 0 | `00000011` |
     | `0100` | 0 | `00000100` |
     | `0101` | 0 | `00000101` |
     | `0110` | 0 | `00000110` |
     | `0111` | 0 | `00000111` |
     | `1000` | 1 | `11111000` |
     | `1001` | 1 | `11111001` |
     | `1010` | 1 | `11111010` |
     | `1011` | 1 | `11111011` |
     | `1100` | 1 | `11111100` |
     | `1101` | 1 | `11111101` |
     | `1110` | 1 | `11111110` |
     | `1111` | 1 | `11111111` |

---

## 📈 Análise

- **Resultados Obtidos**:
  - A saída apresentou a extensão correta do valor de 4 bits para 8 bits, preservando o sinal (MSB).
  - Para valores com MSB = 0, os bits mais significativos da saída foram preenchidos com 0s.
  - Para valores com MSB = 1, os bits mais significativos da saída foram preenchidos com 1s.
- **Observações**:
  - O circuito comportou-se conforme o esperado, sem discrepâncias nos testes.
  - O uso correto do MSB para preencher os bits mais significativos é crucial para preservar a semântica do número.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](src/extensor_sinal_4_to_8.circ)
