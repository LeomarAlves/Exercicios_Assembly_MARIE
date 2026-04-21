# 🖥️ Estudos em Arquitetura de Computadores: Assembly (MARIE)

Este repositório contém a implementação de algoritmos fundamentais escritos na linguagem de montagem (Assembly) para a arquitetura **MARIE** (Machine Architecture that is Really Intuitive and Easy).

O objetivo deste projeto é demonstrar fluência em lógica de programação de baixo nível, manipulação direta de memória, gerenciamento de registradores (Acumulador) e criação de estruturas de controle de fluxo (laços e condicionais) sem o uso de abstrações de linguagens de alto nível.

## 🛠️ Tecnologias e Conceitos Explorados
- **Linguagem:** Assembly (MARIE)
- **Ambiente de Teste:** [MARIE.js Simulator](https://marie.js.org/)
- **Conceitos Aplicados:**
  - Endereçamento Direto e Indireto (`LoadI`, `StoreI`)
  - Saltos Condicionais baseados no estado do Acumulador (`SkipCond`)
  - Manipulação de ponteiros na memória (Navegação em vetores)
  - Operações aritméticas lógicas (simulação de multiplicação e divisão)

---

## 🚀 Exercícios Implementados

### 1. Contador de Ocorrências em Vetor
Percorre um vetor na memória e conta quantas vezes um valor específico (fornecido pelo usuário) aparece.
- **Destaque técnico:** Uso de endereçamento indireto para varrer a memória dinamicamente e implementação de uma estrutura lógica equivalente a um `for-loop` com condicional `if`.

### 2. Inicialização de Vetor com Constante
Preenche sequencialmente um espaço de memória (vetor) com um valor constante fornecido pelo usuário.
- **Destaque técnico:** Uso do comando `StoreI` para escrita dinâmica em endereços de memória calculados em tempo de execução.

### 3. Verificador de Igualdade entre Vetores
Compara dois vetores em posições de memória distintas, validando se são idênticos elemento por elemento. Retorna `1` se iguais e `0` se diferentes.
- **Destaque técnico:** Gerenciamento simultâneo de múltiplos ponteiros de memória (`INI1` e `INI2`) dentro do mesmo ciclo de repetição e lógica de interrupção antecipada (*early return*) ao encontrar divergências.

### 4. Multiplicação por Somas Sucessivas
Calcula o produto de dois números positivos ($A \times B$) utilizando apenas o operador de soma e laços de repetição.
- **Destaque técnico:** Uso de uma das variáveis como contador de decremento para controle preciso do ciclo de iteração da máquina.

### 5. Divisão Inteira (Quociente e Resto)
Implementa a operação de divisão ($A \div B$) através de subtrações sucessivas, retornando o Quociente exato e o Resto da operação.
- **Destaque técnico:** O desafio lógico de gerenciar o Acumulador para não registrar valores negativos, identificando o momento exato de parada do laço (`SkipCond 000`) e preservando a memória para exibir o Resto corretamente.

---

## ⚙️ Como Executar os Códigos

Como o MARIE é uma arquitetura simulada, os arquivos `.mas` (MARIE Assembly) contidos na pasta `src/` são compostos por texto puro.

1. Acesse o simulador online: [MARIE.js](https://marie.js.org/editor/).
2. Copie o conteúdo de qualquer arquivo `.mas` deste repositório.
3. Cole na área de edição do simulador.
4. Clique em **Assemble** para compilar o código.
5. Clique em **Run** (ou ajuste a velocidade em *Speed* e use o *Step* para ver a execução passo a passo).
6. Utilize a caixa de **Inputs** para fornecer os dados quando o programa solicitar.

---

> *"Entender o baixo nível é o primeiro passo para escrever códigos de alto nível mais eficientes."*