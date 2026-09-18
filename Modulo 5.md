<div align="center">
  
# 📘 Módulo 5: Estruturas de Repetição em Python

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---

Bem-vindo ao **Módulo 5** do curso! Neste módulo, você aprenderá como automatizar tarefas repetitivas utilizando as estruturas de repetição `while` e `for`, além de controlar o fluxo de execução com `break` e `continue`.

---

## 📌 Sumário de Conteúdos

1. [🔄 O que são Estruturas de Repetição?](#1--o-que-são-estruturas-de-repetição)
2. [🔁 A Estrutura `while`](#2--a-estrutura-while)
   • Sintaxe básica e controle de loop
   • Exemplo Prático no VS Code
3. [➰ A Estrutura `for` e a Função `range()`](#3--a-estrutura-for-e-a-função-range)
   • Percorrendo sequências e intervalos
   • Exemplo Prático no VS Code
4. [⏹️ Controle de Loop: `break` e `continue`](#4--controle-de-loop-break-e-continue)
   • Interrompendo e pulando iterações
   • Exemplo Prático no VS Code
5. [🛑 Cuidados com Loops Infinitos](#5--cuidados-com-loops-infinitos)
   • Condições de parada
6. [🎯 Exercícios Práticos](#6--exercícios-práticos)
   • Desafios de fixação
7. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. 🔄 O que são Estruturas de Repetição?

Estruturas de repetição (também chamadas de *loops* ou laços) permitem executar um bloco de código várias vezes seguidas enquanto uma condição for verdadeira ou para cada item de uma sequência.

Isso evita a repetição manual de código e permite processar grandes volumes de dados de forma eficiente.

---

## 2. 🔁 A Estrutura `while`

O laço `while` (enquanto) executa um bloco de código **enquanto** uma condição especificada for verdadeira (`True`).

```python
# Sintaxe Básica
while condição:
    # Bloco executado enquanto a condição for True
```

> ⚠️ **Atenção:** É fundamental garantir que a condição se torne falsa em algum momento, caso contrário, o programa entrará em **loop infinito**.

### 💻 Exemplo Prático no VS Code
Crie o arquivo `1_while.py`:

```python
contador = 1

while contador <= 5:
    print(f"Contagem: {contador}")
    contador += 1  # Incrementa a variável para evitar loop infinito

print("Fim do laço while!")
```

---

## 3. ➰ A Estrutura `for` e a Função `range()`

O laço `for` (para) é utilizado para iterar sobre uma sequência (como listas, strings ou um intervalo numérico gerado pela função `range()`).

```python
# Sintaxe com range()
for i in range(inicio, fim, passo):
    # Bloco executado para cada item
```

### Entendendo a função `range()`:
* `range(5)`: gera números de 0 a 4 (5 números).
* `range(1, 6)`: gera números de 1 a 5 (o valor final é exclusivo).
* `range(0, 10, 2)`: gera números pares de 0 a 8 (passo de 2 em 2).

### 💻 Exemplo Prático no VS Code
Crie o arquivo `2_for_range.py`:

```python
print("--- Tabuada do 5 ---")
for i in range(1, 11):
    resultado = 5 * i
    print(f"5 x {i} = {resultado}")
```

---

## 4. ⏹️ Controle de Loop: `break` e `continue`

Podemos alterar o fluxo normal de um loop usando duas instruções especiais:

| Comando | Descrição |
| :---: | :--- |
| `break` | Interrompe e encerra o laço imediatamente. |
| `continue` | Pula a iteração atual e vai para a próxima repetição. |

### 💻 Exemplo Prático no VS Code
Crie o arquivo `3_break_continue.py`:

```python
print("--- Exemplo de continue (Pulando números pares) ---")
for numero in range(1, 10):
    if numero % 2 == 0:
        continue  # Pula o restante do bloco se for par
    print(f"Número ímpar: {numero}")

print("\n--- Exemplo de break (Buscando um número) ---")
for numero in range(1, 100):
    if numero == 7:
        print("Número 7 encontrado! Encerrando o loop.")
        break  # Interrompe o loop completamente
    print(f"Procurando... número atual: {numero}")
```

---

## 5. 🛑 Cuidados com Loops Infinitos

Um loop infinito ocorre quando a condição do `while` nunca se torna `False`.

```python
# ❌ EXEMPLO DE LOOP INFINITO (NÃO EXECUTAR)
# contador = 1
# while contador <= 5:
#     print(contador)
#     # Faltou o incremento: contador += 1
```

**Como interromper:** Se um programa entrar em loop infinito no terminal, pressione `Ctrl + C` para cancelar a execução.

---

## 6. 🎯 Exercícios Práticos

1. **Contagem Regressiva:** Crie um programa usando `while` que faça uma contagem regressiva de 10 até 0 e exiba a mensagem `"Decolagem! 🚀"`.
2. **Soma de Números:** Peça para o usuário digitar números inteiros. O programa deve somar esses números até que o usuário digite `0` (use o `while` com `break`).
3. **Pares no Intervalo:** Crie um programa usando `for` e `range()` que exiba todos os números pares entre 1 e 50.

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |
