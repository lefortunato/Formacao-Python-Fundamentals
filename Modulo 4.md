<div align="center">
  
# 📘 Módulo 4: Estruturas Condicionais em Python

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---

Bem-vindo ao **Módulo 4** do curso! Neste módulo, você aprenderá como fazer o seu programa tomar decisõees lógicas, executando diferentes blocos de código com base em condições especificadas utilizando `if`, `elif` e `else`.

---
## 📌 Sumário de Conteúdos

1. [❓ O que são Estruturas Condicionais?](#1--o-que-são-estruturas-condicionais)
2. [🔀 Estrutura Simples (`if`)](#2--estrutura-simples-if)
3. [🔀 Estrutura Composta (`if` e `else`)](#3--estrutura-composta-if-e-else)
4. [🔀 Estrutura Encadeada (`if`, `elif` e `else`)](#4--estrutura-encadeada-if-elif-e-else)
5. [🪆 Condicionais Aninhadas](#5--condicionais-aninhadas)
6. [⚡ Operador Ternário](#6--operador-ternário)
7. [🎯 Exercícios Práticos](#7--exercícios-práticos)
8. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. ❓ O que são Estruturas Condicionais?

Na vida real, tomamos decisões a todo momento:
* **SE** estiver chovendo, levo um guarda-chuva.
* **SENÃO**, vou de óculos de sol.

Em programação é exatamente igual. As estruturas condicionais avaliam uma expressão booleana (True ou False) e executam um bloco de código apenas se a condição for verdadeira.

⚠️ IMPORTANTE: Indentação no Python
O Python utiliza recuo de texto (4 espaços ou 1 TAB) para definir o que pertence a cada bloco. Respeite sempre a indentação!

---

## 2. 🔀 Estrutura Simples  (`if`)

A instrução `if` (se) executa um bloco de código apenas se a condição for verdadeira. Se for falsa, o programa simplesmente ignora o bloco e segue em frente.

```python
# Sintaxe Básica
if condição:
    # Código executado se a condição for True
```

### 💻 Exemplo Prático no VS Code
Crie o arquivo `1_if_simples.py`:

```python
idade = 20

if idade >= 18:
    print("Você é maior de idade!")
    print("Pode tirar a carteira de habilitação.")

print("Fim do programa.")
```

---

## 3. 🔀 Estrutura Composta (`if` e `else`)

O `else`  (senão) define o que deve ser feito caso a condição do `if` seja **falsa**.

```python
# Sintaxe Básica
if condição:
    # Código se True
else:
    # Código se False
```

### 💻 Exemplo Prático no VS Code
Crie o arquivo `2_if_else.py`:

```python
saldo = 500.0
saque = 700.0

if saldo >= saque:
    saldo -= saque
    print(f"Saque realizado com sucesso! Saldo atual: R$ {saldo:.2f}")
else:
    print("Saldo insuficiente para realizar o saque!")
    print(f"Seu saldo atual é de R$ {saldo:.2f}")
```

---

## 4. 🔀 Estrutura Encadeada (`if`, `elif` e `else`)

Quando temos **mais de duas opções**, usamos o `elif` (abreviaçãoo de *else if*). Você pode ter quantos `elif` precisar entre o `if` e o `else`.

| Instrução | Descrição |
| :---: | :--- |
| `if` | Primeira checagem (obrigatório) |
| `elif` | Checagens intermediárias caso o `if` seja falso (opcional) |
| `else` | Caminho padrão se NENHUMA condição for verdadeira (opcional) |

### 💻 Exemplo Prático no VS Code
Crie o arquivo `3_if_elif_else.py`:

```python
nota = float(input("Digite a nota do aluno (0 a 10): "))

if nota >= 7.0:
    print("Status: Aprovado! 🎉")
elif nota >= 5.0:
    print("Status: Em Recuperação. ⚠️")
else:
    print("Status: Reprovado. ❌?)
```

---

## 5. 🪆 Condicionais Aninhadas

Podemos colocar um `if` dentro de outro `if`. Isso é útil quando uma decisão depende do sucesso de uma decição anterior.

### 💻 Exemplo Prático no VS Code
Crie o arquivo `4_aninhado.py`:

```python
conta_normal = True
saldo = 2000.0
saque = 2500.0
cheque_especial = 1000.0

if conta_normal:
    if saldo >= saque:
        print("Saque realizado com sucesso!")
    elif saque <= (saldo + cheque_especial):
        print("Saque realizado utilizando o Cheque Especial!")
    else:
        print("Saldo e cheque especial insuficientes!")
else:
    print("Conta não reconhecida. Procure o seu gerente.")
```

---

## 6. ⚡ Operador Ternário

É uma forma simplificada e rápida de escrever um `if/else` em apenas uma linha para atribuir um valor a uma variável.

```python
# Sintaxe: valor_se_true if condição else valor_se_false
```

### 💻 Exemplo Prático no VS Code
Crie o arquivo `5_ternario.py`:

```python
saldo = 1000
saque = 500

# Usando o IF Ternário
status = "Sucesso" if saldo >= saque else "Falha"

print(f"Status do saque: {status}")
```
---

## 7. 🎯 Exercícios Práticos

1. **Par ou Ímpar:** Peça para o usuário digitar um número inteiro usando input(). Use o operador de resto (%) e if/else para exibir se o número é Par ou Ímpar.

2. **Aprovador de Empréstimo:** Crie um programa que receba a renda e o valor_parcela. O empréstimo só será aprovado se a parcela for menor ou igual a 30% da renda.

3. **Calculadora de IMC Simplificada:** Receba peso e altura, calcule o IMC (peso / (altura ** 2)) e classifique:

* IMC < 18.5: Abaixo do peso
* IMC entre 18.5 e 24.9: Peso normal
* IMC >= 25.0: Sobrepeso / Obesidade
---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |




