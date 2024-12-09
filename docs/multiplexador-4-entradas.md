# Multiplexador 4x1

## 🔍 Descrição

Dispositivo eletrônico que permite selecionar uma de várias entradas e direcioná-la para uma única saída. Ele funciona como um interruptor digital que escolhe uma das várias opções de entrada de acordo com um sinal de controle. Assim, é uma ferramenta essencial para a transmissão e manipulação eficiente de múltiplos sinais, melhorando o desempenho e reduzindo a quantidade de recursos necessários em muitos sistemas eletrônicos.

## 🖥️ Componentes

- **4 pin de um bit**:
  - 4 inputs, cada um representa um sinal distinto.
- **Portas Lógicas (AND e OR)**:
  - Configuradas para selecionar apenas uma passagem, assim apenas um sinal chega no output.
- **Multiplexador 2x1**:
  - Multiplexador para facilitar o processo de criação.
- **2 Pin de um bit (seletor)**:
  - Pins ultilizados para escolher a saída.  
- **Pin um bit (data)**:
  - Saída correspondente ao sinal escolhido pelo seletor.

## ⚙️ Implementação

1. **Descrição do Circuito**:

   - O circuito ultiliza multiplexador 2x1 (composto por portas AND e OR) para selecionar uma saída, também possivel implementar apenas com as portas lógicas.
   - Começando com os inputs (os sinais que vamos passar), teremos 4 sinais de entrada e apenas 1 saída. Usando o seletor, podemos escolher qual entrada será direcionada para a saída, de acordo com as possibilidades descritas na tabela. Como temos 4 entradas, precisamos de 2 bits para representar essas 4 opções, pois com 2 bits conseguimos contar de 0 a 3, o que nos dá um total de 4 possibilidades de seleção.
  
   - **Tabela Exemplo** 
     | Entradas | seletor |Saida| 
     |----------|---------|-----|
     | _Input0_ |  `00`   |_Input0_|
     | _Input1_ |  `01`   |_Input1_|
     | _Input2_ |  `10`   | _Input2_ |
     | _Input3_ |  `11`   |_Input3_|
     

2. **Imagem do Circuito**:
   
   **Multiplexador 4x1 completo Logisim Evolution:**
     - Ultilizando 2x1.
   
    **Multiplexador 4x1 completo Logisim Evolution:**
     - Apenas portas lógicas.
       
    **Por dentro do componente:**

## 🔬 Testes

1. **Método de Teste**:

   - Descreva como os testes foram realizados (e.g., análise da tabela verdade, simulações).

2. **Resultados dos Testes**:
   - Inclua tabelas ou gráficos com os resultados.

## 📈 Análise

Explique os resultados obtidos e compare-os com o esperado. Adicione observações ou problemas encontrados.

## 📂 Arquivos Relacionados

- [Arquivo do Logisim](../src/nome-do-arquivo.circ)
