# cpu - 8 bits

# Projeto: CPU de Arquitetura Simplificada (8-Bits)

Este repositório contém o desenvolvimento e a simulação de uma **Unidade Central de Processamento (CPU) de 8 bits**, desenvolvida como atividade prática no **Inteli**. [cite_start]O projeto demonstra a implementação física dos ciclos de **Busca (Fetch)** e **Execução (Execute)** através de um circuito lógico funcional[cite: 14].

---

## 🚀 Visão Geral do Sistema

[cite_start]A CPU foi projetada utilizando a ferramenta de simulação **Digital**[cite: 120]. [cite_start]O sistema opera com uma arquitetura de 8 bits para processamento de dados e instruções armazenadas em uma memória ROM[cite: 12, 15].

### Componentes Principais:
* [cite_start]**Unidade Lógica e Aritmética (ALU):** Realiza as operações matemáticas e lógicas fundamentais[cite: 13].
* [cite_start]**Circuito de Controle:** Gerencia a transição entre os estados de busca e execução[cite: 14].
* [cite_start]**Program Counter (PC):** Controla o endereçamento sequencial da memória[cite: 109, 110].
* [cite_start]**Registradores (AC e MQ):** O Acumulador (AC) armazena resultados imediatos, enquanto o MQ lida com multiplicações e divisões[cite: 44, 45].

---

## 🏗️ Detalhamento da Arquitetura

### 1. Program Counter (PC)
[cite_start]Para facilitar o ciclo de busca, foi utilizado o **endereçamento por operandos sequenciais**[cite: 109]. [cite_start]O próximo operando está sempre no endereço imediatamente após o anterior, funcionando de forma análoga a uma pilha[cite: 110].

### 2. Unidade Lógica e Aritmética (ALU)
[cite_start]A ALU implementa 6 operações distintas, selecionadas por um **OpCode** de no mínimo 3 bits[cite: 115].

| Operação | Descrição Técnica | Saída |
| :--- | :--- | :--- |
| **Soma** | [cite_start]AC + N [cite: 27] | [cite_start]AC (8 bits) [cite: 34] |
| **Subtração** | [cite_start]AC - N [cite: 21] | [cite_start]AC (8 bits) [cite: 35] |
| **Multiplicação** | [cite_start]AC * N [cite: 30] | [cite_start]AC (8 LSB) e MQ (8 MSB) [cite: 36] |
| **Divisão** | [cite_start]AC / N [cite: 31] | [cite_start]MQ (Quociente) e AC (Resto) [cite: 37] |
| **Shift Lógico** | [cite_start]Deslocamento de bits para esquerda ou direita [cite: 24] | [cite_start]AC (8 bits) [cite: 38] |

---

##  Demonstração de Execução

O sistema foi validado através de programas carregados na ROM, utilizando palavras de comando de 12 bits para definir a operação e o dado.

* **Soma de 1 + 1:** O sistema busca o valor 1, carrega no AC e, no ciclo seguinte, executa a soma com o operando 1, resultando em 2 no visor do Acumulador.
* **Sincronismo:** A lógica de controle utiliza sinais como `Qe` e `Deq` para garantir que o PC e os registradores não entrem em conflito durante o pulso de clock.

---

## 📺 Apresentação do Projeto

Assista à explicação completa da arquitetura, incluindo a abertura dos subcircuitos do PC e da ALU, no vídeo abaixo:

[![Assista ao vídeo](https://youtu.be/xq7yMoQE9us)

---

##  Critérios de Qualidade Atendidos
* [cite_start]**ALU funcional:** Todas as operações aritméticas e lógicas implementadas.
* [cite_start]**Ciclo de Busca:** Gerenciamento correto de endereçamento e carregamento de instruções.
* [cite_start]**Ciclo de Execução:** Processamento efetivo dos dados pela ALU.

---

## Autor
**Kaian Moura**
