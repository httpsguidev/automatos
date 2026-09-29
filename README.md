# Máquina de Turing

## Etapa 1 — Introdução

### 1. O que é uma Máquina de Turing?

É um modelo matemático criado para explicar de forma precisa o que é computação, foi inspirada no funcionamento de uma máquina de escrever mecânica, ela foi pensada como uma espécie de "supermáquina de escrever" que funciona sobre uma fita de papel infinitamente longa.

A máquina possui um número limitado de estados internos e segue regras bem definidas para cada situação.

### 2. Quais são os principais componentes de uma Máquina de Turing?

- **Fita infinita:** É uma fita dividida em unidades ou quadrados, que serve ao mesmo tempo como entrada, saída, armazenamento de dados e programa.

- **Cabeça de leitura e escrita:** É o mecanismo que se movimenta pela fita. Ele consegue ler o símbolo do quadrado atual, apagar, escrever um novo símbolo e mover-se um quadrado para a esquerda, para a direita ou permanecer parado.

- **Alfabeto de símbolos:** O conjunto de símbolos que podem ser lidos e escritos na fita, pode ser tão simples quanto os símbolos binários e o símbolo de espaço em branco.

- **Conjunto finito de estados:** São as configurações internas em que a máquina pode estar a cada momento, incluindo um estado inicial.

- **Tabela / Função de transição:** Conjunto de regras que orienta o funcionamento da máquina. Com base no estado atual e no símbolo lido na fita, a regra determina qual símbolo deve ser escrito, para onde a cabeça de leitura deve se mover e qual será o próximo estado.

### 3. Qual é a importância das Máquinas de Turing para a computação?

A Máquina de Turing é um dos principais conceitos que servem de base para a Ciência da Computação, pois ela criou um modelo formal para explicar o que é um programa, um computador e quais funções e números podem ser computados.

Também foi responsável pela criação do conceito de Computador Universal, que mostra como uma mesma máquina pode executar diferentes programas, armazenando tanto as instruções quanto os dados.

Além disso, a Máquina de Turing ajudou a estabelecer os limites do que pode ou não ser calculado por um computador, servindo como referência para entender o funcionamento e as possibilidades da computação até os dias de hoje.

### 4. Qual é a relação entre Máquina de Turing e algoritmo?

A relação entre a Máquina de Turing e os algoritmos está na forma como ela permite representar e executar essas instruções de maneira organizada. A tabela de transição e os estados da máquina podem ser usados para representar os passos de um algoritmo, mostrando exatamente o que deve ser feito em cada situação.

Além disso, qualquer algoritmo que possa ser executado em um computador moderno pode ser representado por uma Máquina de Turing. Por isso, quando uma linguagem de programação possui recursos suficientes para realizar os mesmos tipos de tarefas que uma Máquina de Turing, ela é considerada **Turing Complete**.

Isso significa que ela consegue executar qualquer algoritmo que também possa ser processado por uma Máquina de Turing.

---

## Etapa 2 — Simulação

Utilize um software ou simulador de Máquina de Turing indicado pelo professor.

Crie uma máquina capaz de reconhecer palavras da forma:

### 0ⁿ1ⁿ

#### Exemplos aceitos

- `01`
- `0011`
- `000111`
- `00001111`

#### Exemplos rejeitados

- `0`
- `1`
- `001`
- `011`
- `00111`

### Desafio

A máquina deverá verificar se existe a mesma quantidade de símbolos `0` e `1`, seguindo a lógica de funcionamento de uma Máquina de Turing.

---

## Etapa 3 — Registro da Simulação

Após executar a máquina, registre:

- A palavra utilizada como entrada.
- Os estados percorridos.
- O resultado da execução: **ACEITA** ou **REJEITA**.
- Uma captura de tela da simulação.

Realize pelo menos 3 testes:

- 2 entradas que devem ser aceitas.
- 1 entrada que deve ser rejeitada.

### Registro dos testes

| Teste | Entrada | Resultado esperado | Resultado obtido | Estados percorridos |
|:-----:|:-------:|:------------------:|:-----------------:|---------------------|
| **1** | `01` | **ACEITA** | **ACEITA** | `q0 → q1 → q2 → q3 → q1 → q4 → qA` |
| **2** | `0011` | **ACEITA** | **ACEITA** | `q0 → q1 → q2 → q3 → q1 → q2 → q3 → q1 → q4 → qA` |
| **3** | `001` | **REJEITA** | **REJEITA** | `q0 → q1 → q2 → q3 → q1 → q1 → qR` |

### Descrição da Máquina de Turing criada

A Máquina de Turing criada verifica se uma palavra possui a mesma quantidade de símbolos `0` e `1`, seguindo o formato `0ⁿ1ⁿ`. Para isso, a máquina percorre a palavra relacionando cada `0` a um `1` correspondente.

Esse processo é repetido até que todos os símbolos sejam verificados. Caso a quantidade de `0` e `1` seja igual e estejam na ordem correta, a palavra é aceita. Caso contrário, a palavra é rejeitada.

---

## Etapa 4 — Reflexão sobre os Limites Computacionais

### 5. Uma Máquina de Turing consegue resolver qualquer problema?

Explique com suas palavras por que existem problemas que não podem ser resolvidos por algoritmos.

Não, uma Máquina de Turing não consegue resolver qualquer problema, existem problemas em que não é possível criar um algoritmo que sempre encontre uma resposta correta em um número finito de passos, isso acontece porque alguns problemas não podem ser resolvidos apenas seguindo uma sequência de instruções, mesmo que exista bastante tempo e capacidade de processamento, esses problemas são chamados de problemas não computáveis e mostram que existem limites para o que pode ser resolvido por algoritmos.

### 6. Questão Final

**Problema para reflexão:**

Imagine que você recebeu um problema computacional muito complexo. Como saber se ele é apenas difícil de resolver ou se, na verdade, não existe nenhum algoritmo capaz de resolvê-lo para todos os casos?

Explique utilizando os conceitos estudados sobre **Máquinas de Turing, computabilidade e limites computacionais**.

Para saber se um problema é apenas difícil ou se realmente não pode ser resolvido por um algoritmo, é necessário analisar se existe uma Máquina de Turing capaz de chegar a uma resposta para todos os casos possíveis, um problema pode ser muito complexo e exigir bastante tempo e processamento, mas ainda ser computável se existir um algoritmo que consiga resolvê-lo, por outro lado existem problemas em que nenhuma Máquina de Turing consegue encontrar uma solução para todos os casos, esses são considerados problemas não computáveis, mostrando que além das limitações de tempo e processamento, a computação também possui limites sobre quais problemas podem realmente ser resolvidos.
