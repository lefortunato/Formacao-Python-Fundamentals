<div align="center">
  
# 📦 Módulo 2: Variáveis e Tipos de Dados

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---

Bem-vindo ao **Módulo 2**! Aqui você aprenderá como o Python armazena informações na memória do computador e como interagir com o usuário recebendo dados pelo teclado.

---

## 📌 Sumário do Módulo

1. [O que são Variáveis?](#1-o-que-são-variáveis)
2. [Tipos Primitivos de Dados](#2-tipos-primitivos-de-dados)
3. [Descobrindo o Tipo com `type()`](#3-descobrindo-o-tipo-com-type)
4. [Entrada de Dados com `input()`](#4-entrada-de-dados-com-input)
5. [Conversão de Tipos (Casting)](#5-conversão-de-tipos-casting)
6. [Exemplo Prático Completo](#6-exemplo-prático-completo)
7. [Exercícios Práticos](#7-exercícios-práticos)
8. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. O que são Variáveis?

Pense em uma **variável** como uma "caixa com etiqueta" na memória do computador. Você pode guardar uma informação nessa caixa e usá-la a qualquer momento no seu código chamando pelo nome da etiqueta.

### Regras para criar nomes de variáveis:
* Devem começar com letra ou sublinhado (`_`).
* Não podem começar com números.
* Não podem ter espaços (use `_` para separar palavras, padrão conhecido como *snake_case*).
* O Python diferencia maiúsculas de minúsculas (`nome` é diferente de `Nome`).

```python
# Exemplos corretos de variáveis:
nome_usuario = "Maria"
idade = 25
preco_produto = 49.90
```

---

## 2. Tipos Primitivos de Dados

O Python identifica automaticamente o tipo do dado que você armazena. Os 4 tipos básicos são:

| Tipo | Nome no Python | Descrição | Exemplos |
| :--- | :--- | :--- | :--- |
| **Texto** | `str` (String) | Textos envolvidos por aspas simples ou duplas | `"Olá"`, `'Python 3'`, `"123"` |
| **Inteiro** | `int` (Integer) | Números inteiros (positivos ou negativos) | `10`, `0`, `-5`, `2026` |
| **Decimal** | `float` (Floating Point) | Números com casas decimais (usa ponto `.`) | `3.14`, `19.99`, `-0.5` |
| **Booleano** | `bool` (Boolean) | Valores lógicos (Verdadeiro ou Falso) | `True`, `False` |

```python
# 01_tipos_dados.py

nome = "Carlos"       # str
idade = 30            # int
altura = 1.75         # float
estudante = True      # bool
```

---

## 3. Descobrindo o Tipo com `type()`

Você pode usar a função `type()` para verificar qual é o tipo de dado que está armazenado em uma variável.

```python
# 02_verificando_tipos.py

cidade = "São Paulo"
ano = 2026

print(type(cidade))  # Saída: <class 'str'>
print(type(ano))     # Saída: <class 'int'>
```

---

## 4. Entrada de Dados com `input()`

A função `input()` permite que o usuário digite uma informação no terminal enquanto o programa está rodando.

> ⚠️ **ATENÇÃO:** O comando `input()` **SEMPRE** retorna o dado digitado no formato de **texto (`str`)**, mesmo que o usuário digite um número!

```python
# 03_entrada_dados.py

nome = input("Digite o seu nome: ")
print("Olá,", nome, "! Seja bem-vindo(a).")
```

---

## 5. Conversão de Tipos (Casting)

Como o `input()` lê tudo como texto (`str`), precisamos **converter** esse dado caso queiramos fazer cálculos matemáticos com ele.

### Funções de conversão:
* `int()`: Converte para número inteiro.
* `float()`: Converte para número decimal.
* `str()`: Converte para texto.
* `bool()`: Converte para booleano.

```python
# 04_conversao_tipos.py

# Sem conversão (vai concatenar o texto em vez de somar)
idade_texto = input("Digite sua idade: ")
print(type(idade_texto))  # <class 'str'>

# Com conversão correta para inteiro:
idade = int(input("Digite sua idade novamente: "))
proximo_ano = idade + 1
print("No próximo ano você terá:", proximo_ano, "anos.")
```

---

## 6. Exemplo Prático Completo

Crie o arquivo `05_cadastro.py` no VS Code e execute para ver a interação no terminal:

```python
# 05_cadastro.py

print("=== CADASTRO DE ALUNO ===")

nome = input("Digite seu nome completo: ")
idade = int(input("Digite sua idade: "))
altura = float(input("Digite sua altura (ex: 1.75): "))

print("\n=== DADOS CADASTRADOS ===")
print(f"Nome: {nome} (Tipo: {type(nome)})")
print(f"Idade: {idade} anos (Tipo: {type(idade)})")
print(f"Altura: {altura}m (Tipo: {type(altura)})")
```

---

## 7. Exercícios Práticos

Crie uma pasta ou arquivo na pasta `modulo_2/` para resolver os exercícios:

1. **Ficha Pessoal:** Crie um script em Python que solicite o nome, a profissão e a cidade do usuário e exiba uma frase formatada como:  
   `"Olá [Nome], que legal que você trabalha como [Profissão] em [Cidade]!"`.
2. **Calculadora de Idade em Dias:** Crie um script que receba a idade do usuário em anos e exiba aproximadamente quantos dias de vida ele já viveu (considere um ano com 365 dias).

---

### 🟢 Próximo Passo

Com variáveis e tipos dominados, você já está pronto para realizar cálculos e operações complexas! O próximo passo é o **[Módulo 3: Tipos de Operadores](../modulo_3/sumario_modulo_3.md)**.

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |
