# 🎬 Sistema de Reserva de Ingressos (Cinema)

Um projeto desenvolvido em **linguagem C** que simula um sistema de gerenciamento de assentos para uma sala de cinema. O programa é executado diretamente no terminal e permite que o usuário reserve lugares e acompanhe, em tempo real, a ocupação da sala.

---

## 📋 Funcionalidades

* 🎟️ **Compra de ingressos** informando linha e coluna do assento.
* 🪑 **Mapa da sala** atualizado em tempo real.
* ✅ **Verificação de assentos ocupados**, impedindo reservas duplicadas.
* ⚠️ **Validação de entradas inválidas**, evitando erros quando o usuário digita letras no lugar de números.
* 🔄 **Menu interativo**, permitindo realizar várias operações sem reiniciar o programa.

---

## 🧠 Estrutura do Código

O programa foi organizado em duas partes principais:

### `menu()`

Responsável por exibir o menu de opções e receber a escolha do usuário.

Além disso, possui um tratamento de erro para evitar que o programa entre em loop infinito caso sejam digitados caracteres inválidos. Quando isso acontece, o buffer de entrada é limpo utilizando:

```c
while (getchar() != '\n');
```

---

### `main()`

A função principal é responsável por toda a lógica do sistema.

#### Inicialização da sala

A sala é representada por uma matriz bidimensional de **12 linhas** e **15 colunas**, totalizando **180 assentos**.

Todos os lugares começam com o valor **0**, indicando que estão livres.

---

#### Comprar ingresso

Ao selecionar essa opção, o usuário informa:

* Linha (0 a 11)
* Coluna (0 a 14)

O programa realiza três verificações:

1. Se o usuário digitou um valor válido.
2. Se a posição informada existe dentro da matriz.
3. Se o assento escolhido já está ocupado.

Caso todas as verificações sejam aprovadas, o assento recebe o valor **1**, indicando que foi reservado.

---

#### Ver mapa da sala

Percorre toda a matriz utilizando dois laços `for` e exibe o estado atual de cada assento.

Representação:

* **0** → Assento livre
* **1** → Assento ocupado

---

#### Sair

Encerra o programa finalizando o laço principal.

---

## 🛠️ Tecnologias Utilizadas

* Linguagem C
* Biblioteca `stdio.h`
* Biblioteca `stdlib.h`

---

## 📚 Conceitos Praticados

Durante o desenvolvimento deste projeto foram utilizados conceitos fundamentais da linguagem C, como:

* Matrizes bidimensionais
* Funções
* Estruturas condicionais (`if` / `else`)
* Estruturas de repetição (`for` / `while`)
* Validação de entrada do usuário
* Manipulação de variáveis
* Organização de código

---

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone <URL_DO_REPOSITORIO>
```

### 2. Entre na pasta do projeto

```bash
cd nome-do-projeto
```

### 3. Compile o código

```bash
gcc ingressos.c -o ingressos
```

### 4. Execute o programa

#### Linux / macOS

```bash
./ingressos
```

#### Windows

```bash
ingressos.exe
```

---

## 🎯 Objetivo

Este projeto foi desenvolvido como prática dos primeiros conceitos da linguagem C durante a graduação em Ciência da Computação.

O objetivo foi exercitar a lógica de programação por meio da construção de um sistema simples de reserva de assentos, aplicando matrizes, funções, validação de dados e controle de fluxo.

---

## 🔮 Melhorias Futuras

* Exibir os assentos utilizando símbolos (`O` para livre e `X` para ocupado).
* Identificar as fileiras por letras (A, B, C...).
* Permitir o cancelamento de reservas.
* Informar a quantidade de assentos livres e ocupados.
* Salvar as reservas em arquivo para manter os dados após o encerramento do programa.
* Melhorar a interface do terminal.
