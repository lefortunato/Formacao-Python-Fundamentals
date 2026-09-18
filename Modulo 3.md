<div align="center">
  
# 📘 Conteúdo Prático: Módulo 3 – Tipos de Operadores

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---

## 📋 Sumário
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
3. Para cada seção abaixo, crie o arquivo correspondente indicado nos exemplos (ex: `operadores_aritmeticos.py`).
4. Abra o terminal integrado (`Ctrl + '` ou `Cmd + '`) e execute o comando:

   ```bash
   python operadores_aritmeticos.py
   ```

---

## 🌟 **Tipos de Operadores** </br>
Abaixo estão as explicações didáticas e scripts prontos para os alunos executarem no VS Code (você pode criar um arquivo chamado `operadores_aritmeticos.py`).

### 🔢 1. Operadores Aritméticos

Servem para realizar cálculos matemáticos básicos.

```python
# operadores_aritmeticos.py

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

### 🔍 2. Operadores de Comparação

Comparam dois valores e retornam sempre um valor booleano: True (Verdadeiro) ou False (Falso).

```python
# operadores_comparacao.py

x = 5
y = 10

print("Igual a (==):", x == y)        # False
print("Diferente de (!=):", x != y)   # True
print("Maior que (>):", x > y)        # False
print("Menor que (<):", x < y)        # True
print("Maior ou igual (>=):", x >= 5) # True
print("Menor ou igual (<=):", y <= 10)# True
```

### 📝 3. Operadores de Atribuição

Usados para definir ou atualizar o valor de uma variável de forma abreviada.

```python
# operadores_atribuicao.py

numero = 10
print("Valor inicial:", numero)

numero += 5  # Equivalente a: numero = numero + 5
print("Após += 5:", numero) # 15

numero -= 3  # Equivalente a: numero = numero - 3
print("Após -= 3:", numero) # 12

numero *= 2  # Equivalente a: numero = numero * 2
print("Após *= 2:", numero) # 24
```

### 🧠 4. Operadores Lógicos

Servem para combinar duas ou mais expressões de comparação.
* `and:` Retorna True se todas as condições forem verdadeiras.
* `or:` Retorna True se pelo menos uma condição for verdadeira.
* `not:` Inverte o resultado booleano.

```python
# operadores_logicos.py

idade = 20
tem_carteira = True

# Precisa ter 18 anos OU MAIS e TAMBÉM ter carteira
pode_dirigir = (idade >= 18) and tem_carteira
print("Pode dirigir?", pode_dirigir) # True

# Invertendo o valor com NOT
print("Inverso de pode_dirigir:", not pode_dirigir) # False
```

### 🆔 5. Operadores de Identidade

Servem para verificar se dois objetos ocupam a mesma posição na memória do computador (is / is not). Nota: É diferente de comparar apenas o valor (==).

```python
# operadores_identidade.py

lista_a = [1, 2, 3]
lista_b = [1, 2, 3]
lista_c = lista_a

print("Valores são iguais? (==):", lista_a == lista_b) # True (mesmo conteúdo)
print("São o mesmo objeto na memória? (is):", lista_a is lista_b) # False (locais diferentes)
print("São o mesmo objeto na memória? (is):", lista_a is lista_c) # True (mesmo local)
print("NÃO são o mesmo objeto? (is not):", lista_a is not lista_b) # True
```
  
### 🔗 6. Operadores de Associação

Servem para verificar se um elemento está presente dentro de uma sequência (como uma frase, lista ou texto) usando in e not in.

```python
# operadores_identidade.py

lista_a = [1, 2, 3]
lista_b = [1, 2, 3]
lista_c = lista_a

print("Valores são iguais? (==):", lista_a == lista_b) # True (mesmo conteúdo)
print("São o mesmo objeto na memória? (is):", lista_a is lista_b) # False (locais diferentes)
print("São o mesmo objeto na memória? (is):", lista_a is lista_c) # True (mesmo local)
print("NÃO são o mesmo objeto? (is not):", lista_a is not lista_b) # True
```

### 🎯 7. Exercícios Práticos do Módulo

1. **Calculadora Simples**: Crie um script que receba dois números pelo `input()` e exiba a soma, subtração, multiplicação e divisão entre eles.
2. **Validador de Acesso**: Crie um script que verifique se o usuário pode entrar em um evento (requisitos: ter idade >= 18 e ter o nome em uma lista de convidados).

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |





