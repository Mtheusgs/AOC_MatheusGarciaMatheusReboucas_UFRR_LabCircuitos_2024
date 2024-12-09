# Detector de Paridade Ímpar 

## 🔍 Descrição

Este circuito detecta a **paridade ímpar** de um conjunto de bits de entrada. Um número tem paridade ímpar quando a quantidade de bits iguais a 1 no conjunto é ímpar. A saída do circuito será `1` se a paridade for ímpar, e `0` caso contrário.

O objetivo deste exercício é projetar e implementar um circuito combinacional que avalie a paridade de um número binário e forneça a saída correta.

---

## 🖥️ Componentes

Os principais componentes usados no circuito incluem:
- **Portas XOR**: Para calcular a paridade cumulativa entre os bits de entrada.
- **Entradas**: Representam os bits do número a ser avaliado.
- **Saída**: Um único bit indicando a paridade.

---

## ⚙️ Implementação

1. **Descrição do Circuito**:

   - **Entradas**:
     - Ultilizamos um barramento de 4 bits para vetificação .
   - **Saída**:
     - Um único bit que será `1` se a paridade for ímpar, e `0` se for par.
   - **Lógica**:
     - O circuito utiliza portas XOR para realizar a soma binária cumulativa dos bits de entrada. A operação XOR garante que:
       - \( 0 + 0 = 0 \), \( 1 + 1 = 0 \): Resultado par.
       - \( 0 + 1 = 1 \), \( 1 + 0 = 1 \): Resultado ímpar.

2. **Imagem do Circuito**:

   ![Screenshot 2024-12-09 163454](https://github.com/user-attachments/assets/ee405520-d638-45d1-ab1f-a9030d032c1d)


   O circuito implementado no Logisim Evolution possui 4 entradas conectadas sequencialmente a portas XOR, cuja saída final fornece a paridade.

   Como funciona?
   A porta XOR é a pricipal responsável aqui, que quando pega bits iguais passa 0 e diferentes passa 1, então vamos usar um exemplo par e um impar para explicar.

   -0111 :
      Pegamos input 1 e input 2, resultando 0, depois esse resultado com input 3, e 0 + 1 = 1, ou seja ímpar
   -1111:
       Pegamos input 1 e input 2, resultando 0, depois esse resultado com input 3, e ainda temos 0 posteriormente com D barrado por baixo e por cima não temos input 1 e input 2 dando 0 ou seja não conseguimos ultrapassar as portas AND que limitam a solução.

---

## 🔬 Testes

1. **Método de Teste**:

   - A tabela verdade foi usada para validar o funcionamento do circuito.
   - As simulações no Logisim garantiram que os resultados estivessem de acordo com a lógica projetada.

2. **Resultados dos Testes**:

| Entradas (\( I_3 \), \( I_2 \), \( I_1 \), \( I_0 \)) | Saída (\( P \)) |
|------------------------------------------------------|-----------------|
| 0000                                                 | 0               |
| 0001                                                 | 1               |
| 0010                                                 | 1               |
| 0011                                                 | 0               |
| 0100                                                 | 1               |
| 0101                                                 | 0               |
| 0110                                                 | 0               |
| 0111                                                 | 1               |
| 1000                                                 | 1               |
| 1001                                                 | 0               |
| 1010                                                 | 0               |
| 1011                                                 | 1               |
| 1100                                                 | 0               |
| 1101                                                 | 1               |
| 1110                                                 | 1               |
| 1111                                                 | 0               |

---

## 📈 Análise

O circuito produziu os resultados esperados em todas as combinações de entrada, confirmando que a lógica do detector de paridade ímpar foi implementada corretamente. 

https://github.com/user-attachments/assets/d84326f6-385e-4f07-9313-7314fd05fada


### Observações:
- O circuito é eficiente para qualquer número de bits, podendo ser expandido ao adicionar mais portas XOR.
- Não foram encontrados problemas durante a simulação.

---

## 📂 Arquivos Relacionados

- [Arquivo do Logisim Evolution](../src/Detector_impar.circ)
