# Máquina de Estado

## 🔍 Descrição

Uma **Máquina de Estados Finita (FSM - Finite State Machine)** é um modelo de circuito sequencial que transita entre estados predefinidos com base em entradas e, em alguns casos, gera saídas. Neste projeto, implementamos uma máquina de estados no modelo **Moore**, onde as saídas dependem apenas do **estado atual** da máquina, independentemente das entradas.

---

## 🖥️ Componentes

Os principais componentes utilizados no circuito incluem:
- **Flip-Flops**: Para armazenar o estado atual da máquina.
- **Portas Lógicas**: Para implementar as funções de transição de estado e saída.
- **Decodificadores**: Para identificar o estado atual.
- **Entradas e Saídas**:
  - **Entradas**:
    - \( I[n:0] \): Entradas que controlam as transições de estado.
  - **Saídas**:
    -  Leds dependentes do estado atual.

---

## ⚙️ Implementação

### 1. **Descrição do Circuito**

- **Entradas**:
  - \( I \): Entradas que influenciam as transições de estado.
  - \( CLK \): Clock para sincronização do circuito.
- **Saídas**:
  - \( O \): Saída gerada com base no estado atual.
- **Estados**:
  - Um conjunto finito de estados definidos.
- **Transições**:
  - As transições entre estados são controladas pelas entradas.

### 2. **Lógica Implementada**

- A máquina possui três componentes principais:
  1. **Função de Transição de Estado **:
     - Determina o próximo estado com base no estado atual e nas entradas.
  2. **Armazenamento do Estado**:
     - Os estados são armazenados em flip-flops sincronizados pelo clock.
  3. **Função de Saída (\( \lambda \))**:
     - Define as saídas com base no estado atual.

### 3. **Imagem do Circuito**

![Screenshot 2024-12-09 235219](https://github.com/user-attachments/assets/2284ee96-fed6-460e-aed2-a0ae1e35d952)

---

## 🔬 Testes

### 1. **Método de Teste**

- Foram realizados testes para validar:
  1. **Transições de Estado**:
     - Verificação se a máquina muda de estado corretamente com base nas entradas.
  2. **Geração de Saídas**:
     - Análise se as saídas correspondem ao estado atual esperado.
- A máquina foi simulada no Logisim com diferentes sequências de entradas e cenários.

### 2. **Resultados dos Testes**

| Estado Atual | Entrada (\( I \)) | Próximo Estado | Saída (\( O \)) |
|--------------|--------------------|----------------|-----------------|
| \( S_0 \)    | 0                  | \( S_0 \)      | 0               |
| \( S_0 \)    | 1                  | \( S_1 \)      | 0               |
| \( S_1 \)    | 0                  | \( S_2 \)      | 1               |
| \( S_1 \)    | 1                  | \( S_1 \)      | 1               |
| \( S_2 \)    | 0                  | \( S_0 \)      | 0               |
| \( S_2 \)    | 1                  | \( S_3 \)      | 1               |
| \( S_3 \)    | 0                  | \( S_1 \)      | 0               |
| \( S_3 \)    | 1                  | \( S_0 \)      | 1               |

---

## 📈 Análise

### Resultados Obtidos

- A máquina de estados funcionou conforme o esperado:
  - Transições entre os estados foram realizadas corretamente.
  - As saídas refletiram exclusivamente o estado atual, validando o modelo Moore.
- O circuito apresentou estabilidade, com comportamento previsível para todas as combinações de entrada.

### Observações


1. **Expansibilidade**:
   - O circuito pode ser facilmente ampliado para incluir mais estados ou transições.
2. **Problemas Encontrados**:
   - Nenhum problema foi identificado durante os testes.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim](../src/maquinaEstado.circ)
