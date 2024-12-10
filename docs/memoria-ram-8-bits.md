# Memória RAM de 8 Bits

## 🔍 Descrição

O objetivo deste projeto é implementar uma **memória RAM de 8 bits** utilizando componentes básicos como flip-flops e decodificadores. A memória é capaz de armazenar 8 palavras (endereços), cada uma com 8 bits de dados. 

A RAM permite:
- **Operação de Escrita**: Armazenar dados no endereço especificado.
- **Operação de Leitura**: Recuperar os dados armazenados em um endereço.

Este exercício é fundamental para compreender como as memórias funcionam em sistemas digitais.

---

## 🖥️ Componentes

Os principais componentes utilizados incluem:
- **Registradores**: Para armazenar os bits de cada endereço. Criação disponicel nesse repositório [Arquivo logisim Evolution](../docs/banco-de-regsitradores.md)
- **seletor**: Para selecionar o registrador.
- **Multiplexadores/Demultiplexadores**: Para gerenciar os dados entre os endereços.
- **Entradas/Saídas**: 8 bits
  
---

## ⚙️ Implementação

### 1. **Descrição do Circuito**

- **Entradas**:
  - \( D[7:0] \): Dados de entrada (8 bits).
  - \( selector \):permite selecionar um dos 8 registradores.
  - \( ReadWhite \): Sinal que habilita a escrita ou leitura.
  
- **Saídas**:
  - \( Q[7:0] \): Dados de saída (8 bits), correspondentes ao endereço lido.
  - 
- **Lógica**:
  - O endereço fornecido é decodificado, ativando o o registrador correspondente.
  - Quando \( ReadWhite = 1 \), os dados na entrada (\( D[7:0] \)) são armazenados no endereço selecionado.
  - Quando \( ReadWhite = 0 \), os dados armazenados no endereço especificado são enviados para a saída (\( Q[7:0] \)).

### 2. **Imagem do Circuito**

![Screenshot 2024-12-09 205308](https://github.com/user-attachments/assets/fd579eb5-2f30-427b-a8e7-2faa68413e28)

---

## 🔬 Testes

### 1. **Método de Teste**

- O circuito foi testado para verificar o armazenamento e recuperação de dados:
  - Escrever valores em cada endereço.
  - Ler os valores armazenados e compará-los com o esperado.

### 2. **Resultados dos Testes**

| \( Seletor[2:0] \) | \( D[7:0] \) Escrito | \( Q[7:0] \) Lido | \( ReadWhite \) | \( ReadWhite \) |
|-----------------|----------------------|-------------------|----------|----------|
| 000             | 10101010            | 10101010          | 0        | 1        |
| 001             | 11001100            | 11001100          | 0       | 1       |
| 010             | 11110000            | 11110000          | 0        | 1       |
| 011             | 00001111            | 00001111          | 0        | 1        |
| 100             | 01010101            | 01010101          | 0       | 1        |
| 101             | 10011001            | 10011001          | 0        | 1        |
| 110             | 00111100            | 00111100          | 0        | 1        |
| 111             | 00000000            | 00000000          | 0        | 1        |

---

## 📈 Análise

### Resultados Obtidos

- A memória RAM funcionou corretamente:
  - Os dados foram armazenados nos endereços especificados quando \( ReadWrite = 0 \).
  - Os dados foram recuperados corretamente quando \( ReadWrite = 0 \).

### Observações

1. **Sincronização**:
   - O circuito deve ser sincronizado com um clock, especialmente em sistemas maiores.
2. **Expansibilidade**:
   - O projeto pode ser ampliado para maior capacidade (e.g., 16 ou 32 palavras)
3. **Problemas Encontrados**:
   - Nenhum problema foi identificado durante os testes no Logisim Evolution.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](../src/MemoriaRam.circ)
