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
- **Flip-Flops (D ou SR)**: Para armazenar os bits de cada endereço.
- **Decodificador**: Para selecionar o endereço durante as operações de leitura/escrita.
- **Multiplexadores/Demultiplexadores**: Para gerenciar os dados entre os endereços.
- **Entradas/Saídas**:
  - Entradas:
    - \( D[7:0] \): Dados de 8 bits a serem armazenados.
    - \( Addr[2:0] \): Endereço de 3 bits para acessar as palavras.
    - \( WE \): Sinal de escrita (Write Enable).
    - \( RE \): Sinal de leitura (Read Enable).
  - Saídas:
    - \( Q[7:0] \): Dados lidos do endereço especificado.

---

## ⚙️ Implementação

### 1. **Descrição do Circuito**

- **Entradas**:
  - \( D[7:0] \): Dados de entrada (8 bits).
  - \( Addr[2:0] \): Endereço de 3 bits (permite selecionar até 8 endereços).
  - \( WE \): Sinal que habilita a escrita nos flip-flops.
  - \( RE \): Sinal que habilita a leitura dos flip-flops.
- **Saídas**:
  - \( Q[7:0] \): Dados de saída (8 bits), correspondentes ao endereço lido.
- **Lógica**:
  - O endereço fornecido (\( Addr \)) é decodificado, ativando o banco de flip-flops correspondente.
  - Quando \( WE = 1 \), os dados na entrada (\( D[7:0] \)) são armazenados no endereço selecionado.
  - Quando \( RE = 1 \), os dados armazenados no endereço especificado são enviados para a saída (\( Q[7:0] \)).

### 2. **Imagem do Circuito**

![Circuito da Memória RAM de 8 Bits](../assets/ram_8bits.png)

---

## 🔬 Testes

### 1. **Método de Teste**

- O circuito foi testado para verificar o armazenamento e recuperação de dados:
  - Escrever valores em cada endereço.
  - Ler os valores armazenados e compará-los com o esperado.
- Testes foram realizados no Logisim com diferentes combinações de \( Addr, WE, RE \).

### 2. **Resultados dos Testes**

| \( Addr[2:0] \) | \( D[7:0] \) Escrito | \( Q[7:0] \) Lido | \( WE \) | \( RE \) |
|-----------------|----------------------|-------------------|----------|----------|
| 000             | 10101010            | 10101010          | 1        | 1        |
| 001             | 11001100            | 11001100          | 1        | 1        |
| 010             | 11110000            | 11110000          | 1        | 1        |
| 011             | 00001111            | 00001111          | 1        | 1        |
| 100             | 01010101            | 01010101          | 1        | 1        |
| 101             | 10011001            | 10011001          | 1        | 1        |
| 110             | 00111100            | 00111100          | 1        | 1        |
| 111             | 00000000            | 00000000          | 1        | 1        |

---

## 📈 Análise

### Resultados Obtidos

- A memória RAM funcionou corretamente:
  - Os dados foram armazenados nos endereços especificados quando \( WE = 1 \).
  - Os dados foram recuperados corretamente quando \( RE = 1 \).
- O circuito respondeu de forma precisa às combinações de sinais \( WE \) e \( RE \).

### Observações

1. **Sincronização**:
   - O circuito deve ser sincronizado com um clock, especialmente em sistemas maiores.
2. **Expansibilidade**:
   - O projeto pode ser ampliado para maior capacidade (e.g., 16 ou 32 palavras) ajustando o número de endereços e flip-flops.
3. **Problemas Encontrados**:
   - Nenhum problema foi identificado durante os testes no Logisim.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim](../src/MemoriaRam.circ)
