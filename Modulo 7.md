<div align="center">
  
# 📘 Módulo 7: Dicionários e Conjuntos em Python (`dict` e `set`)

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

Bem-vindo ao **Módulo 7** do curso! Neste módulo, você aprenderá a trabalhar com duas estruturas de dados fundamentais em Python: os **Dicionários** (para armazenar dados no formato chave-valor) e os **Conjuntos** (para manipular coleções de elementos únicos e realizar operações matemáticas de conjuntos).

---

## 📌 Sumário de Conteúdos

1. [📖 Dicionários (`dict`) - Estruturas Chave-Valor](#1--dicionários-dict---estruturas-chave-valor)
   * [Criação e Acesso a Elementos](#criação-e-acesso-a-elementos)
   * [Métodos Principais (`get`, `keys`, `values`, `items`)](#métodos-principais-get-keys-values-items)
   * [Adicionando e Modificando Dados](#adicionando-e-modificando-dados)
2. [🎯 Conjuntos (`set`) - Elementos Únicos](#2--conjuntos-set---elementos-únicos)
   * [Características e Remoção de Duplicatas](#características-e-remoção-de-duplicatas)
   * [Operações de Conjuntos (União, Interseção, Diferença)](#operações-de-conjuntos-união-interseção-diferença)
3. [🔄 Iterando sobre Dicionários e Conjuntos](#3--iterando-sobre-dicionários-e-conjuntos)
4. [💻 Exemplo Prático Integrado no VS Code](#4--exemplo-prático-integrado-no-vs-code)
5. [🎯 Exercícios Práticos](#5--exercícios-práticos)
6. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. 📖 Dicionários (`dict`) - Estruturas Chave-Valor

Dicionários são coleções mutáveis e ordenadas (a partir do Python 3.7) que armazenam dados no formato de pares **`chave: valor`**. São delimitados por chaves `{}`.

### Criação e Acesso a Elementos

```python
# Criando um dicionário
aluno = {
    "nome": "Carlos",
    "idade": 22,
    "curso": "Engenharia de Software",
    "nota_final": 8.5
}

# Acessando valores através da chave
print(aluno["nome"])        # "Carlos"
print(aluno["nota_final"])  # 8.5
```

### Métodos Principais (`get`, `keys`, `values`, `items`)

* `.get(chave, valor_padrao)`: Acessa o valor de forma segura, evitando erros caso a chave não exista.
* `.keys()`: Retorna todas as chaves do dicionário.
* `.values()`: Retorna todos os valores do dicionário.
* `.items()`: Retorna pares `(chave, valor)` como tuplas.

```python
# Acesso seguro com .get()
print(aluno.get("email", "Email não cadastrado"))  # Retorna o valor padrão em vez de quebrar o programa

# Obtendo chaves e valores
print(list(aluno.keys()))    # ['nome', 'idade', 'curso', 'nota_final']
print(list(aluno.values()))  # ['Carlos', 22, 'Engenharia de Software', 8.5]
```

### Adicionando e Modificando Dados

```python
# Alterando valor existente
aluno["nota_final"] = 9.0

# Adicionando nova chave-valor
aluno["matriculado"] = True

# Removendo uma chave
del aluno["idade"]
```

---

## 2. 🎯 Conjuntos (`set`) - Elementos Únicos

Conjuntos são coleções não ordenadas e não indexadas que **não permitem elementos duplicados**. São ideais para eliminar itens repetidos de uma lista ou para testes de pertencimento rápido.

### Características e Remoção de Duplicatas

```python
# Criando um conjunto
frutas = {"maçã", "banana", "laranja", "maçã"}
print(frutas)  # {"maçã", "banana", "laranja"} - 'maçã' duplicada foi removida automaticamente!

# Removendo duplicatas de uma lista rapidamente
numeros = [1, 2, 2, 3, 4, 4, 4, 5]
numeros_unicos = list(set(numeros))
print(numeros_unicos)  # [1, 2, 3, 4, 5]
```

### Operações de Conjuntos (União, Interseção, Diferença)

```python
conjunto_a = {1, 2, 3, 4}
conjunto_b = {3, 4, 5, 6}

# União (|) - junta todos sem repetir
print(conjunto_a | conjunto_b)  # {1, 2, 3, 4, 5, 6}

# Interseção (&) - apenas o que está em ambos
print(conjunto_a & conjunto_b)  # {3, 4}

# Diferença (-) - o que está no A mas não no B
print(conjunto_a - conjunto_b)  # {1, 2}
```

---

## 3. 🔄 Iterando sobre Dicionários e Conjuntos

### Percorrendo Dicionários

```python
produto = {"nome": "Teclado", "preco": 150.0, "estoque": 20}

# Percorrendo chaves e valores simultaneamente
for chave, valor in produto.items():
    print(f"{chave.capitalize()}: {valor}")
```

### Percorrendo Conjuntos

```python
linguagens = {"Python", "JavaScript", "C++"}

for lang in linguagens:
    print(f"Linguagem: {lang}")
```

---

## 4. 💻 Exemplo Prático Integrado no VS Code

Crie o arquivo `cadastro_produtos.py`:

```python
# Sistema simples de cadastro e busca de produtos

catalogo = {}

while True:
    print("\n--- SISTEMA DE PRODUTOS ---")
    print("1. Cadastrar Produto")
    print("2. Buscar Produto")
    print("3. Listar Todos os Produtos")
    print("4. Sair")
    
    opcao = input("Escolha uma opção (1-4): ").strip()
    
    if opcao == "1":
        codigo = input("Digite o código do produto: ").strip()
        nome = input("Digite o nome do produto: ").strip()
        preco = float(input("Digite o preço (R$): "))
        
        catalogo[codigo] = {"nome": nome, "preco": preco}
        print(f"Produto '{nome}' cadastrado com sucesso!")
        
    elif opcao == "2":
        codigo = input("Digite o código para busca: ").strip()
        produto = catalogo.get(codigo)
        
        if produto:
            print(f"\nProduto Encontrado:")
            print(f"  Nome: {produto['nome']}")
            print(f"  Preço: R$ {produto['preco']:.2f}")
        else:
            print("Produto não localizado no sistema.")
            
    elif opcao == "3":
        if not catalogo:
            print("Nenhum produto cadastrado.")
        else:
            print("\n--- CATÁLOGO DE PRODUTOS ---")
            for cod, info in catalogo.items():
                print(f"Código: {cod} | Nome: {info['nome']} | Preço: R$ {info['preco']:.2f}")
                
    elif opcao == "4":
        print("Encerrando o sistema...")
        break
    else:
        print("Opção inválida! Tente novamente.")
```

---

## 5. 🎯 Exercícios Práticos

1. **Dicionário de Pessoas:** Crie um programa que leia o `nome`, `idade` e `cidade` de uma pessoa e guarde em um dicionário. Exiba os dados formatados na tela.
2. **Contador de Vogais:** Escreva uma função que receba uma frase e retorne um dicionário contendo a contagem de cada vogal (`a`, `e`, `i`, `o`, `u`).
3. **Análise de Turmas com Conjuntos:** Crie dois conjuntos representando os alunos matriculados na disciplina A e na disciplina B. Calcule e mostre:
   * Quais alunos estão matriculados em **ambas** as disciplinas.
   * Quais alunos estão matriculados em **apenas uma** das disciplinas.

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |
