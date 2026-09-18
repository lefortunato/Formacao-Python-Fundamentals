<div align="center">
  
# 📘  Módulo 6: Estruturas de Dados em Python (Listas e Tuplas)

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

Bem-vindo ao **Módulo 6** do curso! Neste módulo, você aprenderá a armazenar e manipular múltiplos valores em uma única variável utilizando as duas estruturas de dados sequenciais mais fundamentais do Python: **Listas** e **Tuplas**.

---

## 📌 Sumário de Conteúdos

1. [📦 O que são Estruturas de Dados?](#1--o-que-são-estruturas-de-dados)
2. [📜 Listas (`list`) - Sequências Mutáveis](#2--listas-list---sequências-mutáveis)
   * [Criação e Acesso por Índices](#criação-e-acesso-por-índices)
   * [Métodos Principais (`append`, `insert`, `pop`, `remove`)](#métodos-principais-append-insert-pop-remove)
   * [Fatiamento de Listas (*Slicing*)](#fatiamento-de-listas-slicing)
3. [🔒 Tuplas (`tuple`) - Sequências Imutáveis](#3--tuplas-tuple---sequências-imutáveis)
   * [Definição e Vantagens](#definição-e-vantagens)
   * [Desempacotamento de Tuplas](#desempacotamento-de-tuplas)
4. [🔄 Iterando sobre Listas e Tuplas com `for`](#4--iterando-sobre-listas-e-tuplas-com-for)
5. [💻 Exemplo Prático Integrado no VS Code](#5--exemplo-prático-integrado-no-vs-code)
6. [🎯 Exercícios Práticos](#6--exercícios-práticos)
7. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. 📦 O que são Estruturas de Dados?

Até agora, aprendemos a guardar apenas um valor por variável (um número, um texto ou um booleano). As **estruturas de dados** nos permitem organizar, agrupar e manipular conjuntos inteiros de dados sob um único nome de variável.

---

## 2. 📜 Listas (`list`) - Sequências Mutáveis

Listas são coleções ordenadas de elementos delimitadas por colchetes `[]`. Elas são **mutáveis**, o que significa que você pode adicionar, remover ou alterar elementos a qualquer momento.

### Criação e Acesso por Índices

Em Python, o primeiro elemento sempre fica na posição **0**.

```python
# Criando uma lista
frutas = ["maçã", "banana", "laranja", "uva"]

# Acessando elementos por índice
print(frutas[0])   # "maçã"
print(frutas[2])   # "laranja"
print(frutas[-1])  # "uva" (último elemento)
```

### Métodos Principais (`append`, `insert`, `pop`, `remove`)

* `append(valor)`: Adiciona um item ao final da lista.
* `insert(índice, valor)`: Insere um item em uma posição específica.
* `pop(índice)`: Remove e retorna o item do índice indicado (ou o último, se não informado).
* `remove(valor)`: Remove a primeira ocorrência do valor indicado.

```python
numeros = [10, 20, 30]

numeros.append(40)         # [10, 20, 30, 40]
numeros.insert(1, 15)      # [10, 15, 20, 30, 40]
numeros.pop()              # Remove o 40 -> [10, 15, 20, 30]
numeros.remove(20)         # Remove o 20 -> [10, 15, 30]
```

### Fatiamento de Listas (*Slicing*)

Permite extrair partes de uma lista utilizando a sintaxe `lista[início:fim:passo]`.

```python
letras = ["a", "b", "c", "d", "e", "f"]

print(letras[1:4])  # ["b", "c", "d"] (do índice 1 até antes do 4)
print(letras[:3])   # ["a", "b", "c"] (do início até o índice 2)
print(letras[3:])   # ["d", "e", "f"] (do índice 3 até o final)
```

---

## 3. 🔒 Tuplas (`tuple`) - Sequências Imutáveis

Tuplas são coleções ordenadas delimitadas por parênteses `()`. A principal característica da tupla é ser **imutável**: uma vez criada, você **não pode** alterar, adicionar ou remover elementos.

```python
# Criando uma tupla
coordenadas = (-23.5505, -46.6333)
meses = ("Janeiro", "Fevereiro", "Março")

# Acesso é igual ao de listas
print(meses[0])  # "Janeiro"

# Tentar alterar gera ERRO:
# meses[0] = "Dezembro"  -> TypeError!
```

### Desempacotamento de Tuplas

Você pode atribuir os valores de uma tupla diretamente a múltiplas variáveis de uma só vez:

```python
ponto = (10, 20)
x, y = ponto

print(f"Eixo X: {x}, Eixo Y: {y}")
```

---

## 4. 🔄 Iterando sobre Listas e Tuplas com `for`

Podemos percorrer todos os elementos de uma lista ou tupla utilizando o laço `for`.

```python
alunos = ["Ana", "Bruno", "Carla", "Daniel"]

for aluno in alunos:
    print(f"Aluno cadastrado: {aluno}")
```

Se precisar do índice e do valor ao mesmo tempo, use `enumerate()`:

```python
for indice, aluno in enumerate(alunos, start=1):
    print(f"{indice}º lugar: {aluno}")
```

---

## 5. 💻 Exemplo Prático Integrado no VS Code

Crie o arquivo `gerenciador_compras.py`:

```python
# Sistema simples de lista de compras

carrinho = []

while True:
    print("\n--- MENU DE COMPRAS ---")
    print("1. Adicionar item")
    print("2. Remover item")
    print("3. Ver carrinho")
    print("4. Sair")
    
    opcao = input("Escolha uma opção (1-4): ")
    
    if opcao == "1":
        item = input("Digite o nome do produto: ").strip()
        carrinho.append(item)
        print(f"'{item}' adicionado com sucesso!")
    elif opcao == "2":
        item = input("Digite o nome do produto a remover: ").strip()
        if item in carrinho:
            carrinho.remove(item)
            print(f"'{item}' removido!")
        else:
            print("Item não encontrado no carrinho.")
    elif opcao == "3":
        if not carrinho:
            print("Seu carrinho está vazio.")
        else:
            print("\nItens no Carrinho:")
            for i, prod in enumerate(carrinho, start=1):
                print(f"  {i}. {prod}")
    elif opcao == "4":
        print("Saindo do sistema. Boas compras!")
        break
    else:
        print("Opção inválida! Tente novamente.")
```

---

## 6. 🎯 Exercícios Práticos

1. **Maior e Menor Número:** Crie uma lista com 5 números inteiros fornecidos pelo usuário. Em seguida, exiba a lista completa, o maior valor (`max()`) e o menor valor (`min()`).
2. **Filtro de Pares:** Dada a lista `numeros = [12, 5, 8, 19, 20, 3, 7, 14]`, crie uma nova lista contendo apenas os números pares e exiba o resultado.
3. **Conversor de Tupla para Lista:** Crie uma tupla com os nomes dos 7 dias da semana. Peça ao usuário para escolher um dia e altere o nome desse dia para "HOJE" (Dica: converta a tupla em lista usando `list()`, faça a alteração e converta de volta com `tuple()`).

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |
