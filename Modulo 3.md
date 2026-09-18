<div align="center">
  
# 📘 Módulo 3: Tipos de Operadores em Python

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---
Bem-vindo ao **Módulo 3** do curso! Neste módulo, você aprenderá como manipular dados, realizar cálculos matemáticos, comparar valores e tomar decisões lógicas utilizando os operadores do Python.

## 📌 Sumário de Conteúdos

1. [🔢 Operadores Aritméticos](#1-operadores-aritméticos)
2. [🔍 Operadores de Comparação](#2-operadores-de-comparação)
3. [📝 Operadores de Atribuição](#3-operadores-de-atribuição)
4. [🧠 Operadores Lógicos](#4-operadores-lógicos)
5. [🆔 Operadores de Identidade](#5-operadores-de-identidade)
6. [🔗 Operadores de Associação](#6-operadores-de-associação)
7. [🎯 Exercícios Práticos do Módulo](#7-exercícios-práticos-do-módulo)
8. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)
---

## 🛠️ Como Executar os Exemplos no VS Code

1. Abra o **VS Code**.
2. Crie uma pasta chamada `modulo_3_operadores`.
3. Para cada seção abaixo, crie o arquivo correspondente indicado nos exemplos (ex: `01_aritmeticos.py`).
4. Abra o terminal integrado (`Ctrl + '` ou `Cmd + '`) e execute o comando:
   ```bash
   python 01_aritmeticos.py
   ```

---

### 1. Operadores Aritméticos

Usados para executar operações matemáticas clássicas.

#### Tabela de Operadores Aritméticos

| Operador | Nome | Descrição | Exemplo |
| :--- | :--- | :--- | :--- |
| `+` | Adição | Soma dois valores | `5 + 3` (8) |
| `-` | Subtração | Subtrai o segundo valor do primeiro | `5 - 3` (2) |
| `*` | Multiplicação | Multiplica dois valores | `5 * 3` (15) |
| `/` | Divisão | Divide e retorna resultado em `float` | `5 / 2` (2.5) |
| `//` | Divisão Inteira | Divide e descarta as casas decimais | `5 // 2` (2) |
| `%` | Módulo / Resto | Retorna o resto da divisão inteira | `5 % 2` (1) |
| `**` | Exponenciação | Eleva o valor à potência | `2 ** 3` (8) |

#### Exemplo Prático (`01_aritmeticos.py`)

```python
a = 10
b = 3

print("Soma (+):", a + b)           # 13
print("Subtração (-):", a - b)      # 7
print("Multiplicação (*):", a * b)  # 30
print("Divisão (/):", a / b)        # 3.333...
print("Divisão Inteira (//):", a // b) # 3 (descarta as casas decimais)
print("Módulo/Resto (%):", a % b)   # 1 (resto da divisão)
print("Exponenciação (**):", a ** b)# 1000 (10 elevado a 3)
```

---

### 2. Operadores de Comparação

Comparam dois valores e sempre retornam um resultado booleano (`True` ou `False`).

#### Tabela de Operadores de Comparação

| Operador | Nome | Exemplo | Resultado |
| :--- | :--- | :--- | :--- |
| `==` | Igual a | `10 == 10` | `True` |
| `!=` | Diferente de | `10 != 5` | `True` |
| `>` | Maior que | `10 > 5` | `True` |
| `<` | Menor que | `10 < 5` | `False` |
| `>=` | Maior ou igual a | `10 >= 10` | `True` |
| `<=` | Menor ou igual a | `5 <= 10` | `True` |

#### Exemplo Prático (`02_comparacao.py`)

```python
x = 5
y = 10

print("Igual a (==):", x == y)         # False
print("Diferente de (!=):", x != y)    # True
print("Maior que (>):", x > y)         # False
print("Menor que (<):", x < y)         # True
print("Maior ou igual (>=):", x >= 5)  # True
print("Menor ou igual (<=):", y <= 10) # True
```

---

### 3. Operadores de Atribuição

Servem para definir ou atualizar o valor de uma variável.

#### Tabela de Operadores de atribuição

| Operador | Equivalência | Descrição | Exemplo (`x = 10`) | Resultado |
| :---: | :---: | :--- | :---: | :---: |
| `=` | `x = 10` | Atribui um valor à variável | `x = 10` | `10` |
| `+=` | `x = x + 5` | Soma e atualiza a variável | `x += 5` | `15` |
| `-=` | `x = x - 3` | Subtrai e atualiza a variável | `x -= 3` | `7` |
| `*=` | `x = x * 2` | Multiplica e atualiza a variável | `x *= 2` | `20` |
| `/=` | `x = x / 2` | Divide e atualiza a variável | `x /= 2` | `5.0` |
| `//=` | `x = x // 3` | Aplica divisão inteira e atualiza | `x //= 3` | `3` |
| `%=` | `x = x % 3` | Guarda o resto da divisão e atualiza | `x %= 3` | `1` |
| `**=` | `x = x ** 2` | Eleva à potência e atualiza | `x **= 2` | `100` |

#### Exemplo Prático (`03_atribuicao.py`)

```python
print("--- OPERADORES DE ATRIBUIÇÃO ---")
saldo = 100
print("Saldo inicial:", saldo)

saldo += 50  # Equivalente a: saldo = saldo + 50
print("Após saldo += 50:", saldo)

saldo -= 30  # Equivalente a: saldo = saldo - 30
print("Após saldo -= 30:", saldo)

saldo *= 2   # Equivalente a: saldo = saldo * 2
print("Após saldo *= 2:", saldo)
```

---

### 4. Operadores Lógicos

Os operadores lógicos são fundamentais para construir condições no código. Eles avaliam expressões e retornam um valor booleano (`True` ou `False`).

#### Conceitos Básicos:
* **`and` (E)**: Retorna `True` **apenas se todas** as expressões forem verdadeiras.
* **`or` (OU)**: Retorna `True` se **pelo menos uma** das expressões for verdadeira.
* **`not` (Negação)**: Inverte o valor lógico. Se algo for verdadeiro, torna-se `False`; se for falso (ou vazio), torna-se `True`.

#### Exemplos Detalhados e Práticos (`04_logicos.py`)

Crie o arquivo `04_logicos.py` no VS Code para rodar os exemplos abaixo:

```python
# --- 1. EXEMPLO COM O OPERADOR 'and' ---
# O operador 'and' exige que AMBAS as condições sejam True.

saldo = 1000
saque = 200
limite = 100

# Condição 1: saldo >= saque (1000 >= 200) -> True
# Condição 2: saque <= limite (200 <= 100) -> False
# Resultado: True and False -> False
resultado_and = saldo >= saque and saque <= limite
print("Resultado com AND (saldo >= saque e saque <= limite):", resultado_and)
# Output: False


# --- 2. EXEMPLO COM O OPERADOR 'or' ---
# O operador 'or' exige que PELO MENOS UMA das condições seja True.

saldo = 1000
saque = 200
limite = 100

# Condição 1: saldo >= saque (1000 >= 200) -> True
# Condição 2: saque <= limite (200 <= 100) -> False
# Resultado: True or False -> True
resultado_or = saldo >= saque or saque <= limite
print("Resultado com OR (saldo >= saque ou saque <= limite):", resultado_or)
# Output: True


# --- 3. EXEMPLO COM O OPERADOR 'not' (NEGAÇÃO) ---
# O 'not' inverte o valor de uma expressão ou avalia a "falsidade" de um valor (como listas ou textos vazios).

contatos_emergencia = [] # Lista vazia (em Python, valores vazios são avaliados como False)

# Negação de expressão matemática: 1000 > 1500 é False -> not False vira True
print("not 1000 > 1500:", not 1000 > 1500)  # True

# Negação de coleção vazia: contatos_emergencia é vazia (False) -> not False vira True
print("not contatos_emergencia:", not contatos_emergencia)  # True

# Negação de texto preenchido: "saque 1500;" tem conteúdo (True) -> not True vira False
print("not 'saque 1500;':", not "saque 1500;")  # False

# Negação de texto vazio: "" é uma string vazia (False) -> not False vira True
print("not '':", not "")  # True
```

---

### 5. Operadores de Identidade

Comparam se dois objetos ocupam a **mesma posição na memória** do computador.

* **`is`**: Retorna `True` se forem o mesmo objeto.
* **`is not`**: Retorna `True` se **não** forem o mesmo objeto.

#### Exemplo Prático (`05_identidade.py`)

```python
lista_1 = [1, 2, 3]
lista_2 = [1, 2, 3]
lista_3 = lista_1

print("--- OPERADORES DE IDENTIDADE ---")
print("lista_1 == lista_2 (mesmo conteúdo):", lista_1 == lista_2) # True
print("lista_1 is lista_2 (mesmo local na memória):", lista_1 is lista_2) # False
print("lista_1 is lista_3 (mesmo local na memória):", lista_1 is lista_3) # True
```

---

### 6. Operadores de Associação

Verificam se um elemento está presente em uma sequência (strings, listas, tuplas, etc.).

* **`in`**: Retorna `True` se o valor estiver presente.
* **`not in`**: Retorna `True` se o valor **não** estiver presente.

#### Exemplo Prático (`06_associacao.py`)

```python
linguagem = "Python"
tecnologias = ["Python", "VS Code", "Git", "GitHub"]

print("--- OPERADORES DE ASSOCIAÇÃO ---")
print("'Py' está em linguagem?", "Py" in linguagem)             # True
print("'HTML' está na lista de tecnologias?", "HTML" in tecnologias) # False
print("'Java' NÃO está na lista?", "Java" not in tecnologias)     # True
```

---

### 7. Exercícios Práticos do Módulo

1. **Calculadora de Saque Bancário**: Crie um script que receba o saldo da conta e o valor do saque desejado. Exiba no console se o saque é permitido usando operadores lógicos (`saldo >= saque` e `saque <= limite_diario`).
2. **Validador de Lista Vazia**: Crie um script que defina uma lista de tarefas. Use o operador `not` para exibir uma mensagem avisando o usuário se a lista estiver vazia.

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |





