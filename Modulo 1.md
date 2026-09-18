<div align="center">
  
# 📘 Módulo 1: Introdução & Configuração

![Status](https://img.shields.io/badge/Status-Concluído-success)
![Metodologia](https://img.shields.io/badge/Python-blue)
![Nível](https://img.shields.io/badge/Nível-Iniciante-yellow)

</div>

---

Bem-vindo ao **Módulo 1**! O objetivo deste módulo é deixar o seu ambiente de desenvolvimento pronto e executar o seu primeiro programa em Python.

---

## 📌 Sumário do Módulo

1. [O que é o VS Code e por que usamos?](#1-o-que-é-o-vs-code)
2. [Instalando a Extensão do Python no VS Code](#2-instalando-a-extensão-do-python)
3. [Instalando o Python pelo Terminal](#3-instalando-o-python-pelo-terminal)
4. [Criando e Executando o "Hello World"](#4-seu-primeiro-código-hello-world)
5. [Exercício Prático](#5-exercício-prático)
6. [🔗 Como Contribuir / Contato](#-como-contribuir--contato)

---

## 1. O que é o VS Code?

O **VS Code (Visual Studio Code)** é um editor de código-fonte gratuito e leve criado pela Microsoft. Ele nos ajuda a escrever programas com recursos como:
* Destaque de cores no código (sintaxe).
* Sugestão e autocompletar de comandos.
* Terminal integrado para rodar nossos scripts.

---

## 2. Instalando a Extensão do Python

Para que o VS Code entenda a linguagem Python:
1. Abra o VS Code.
2. No menu lateral esquerdo, clique no ícone de **Extensões** (ou aperte `Ctrl + Shift + X` / `Cmd + Shift + X`).
3. Na barra de pesquisa, digite `Python`.
4. Clique na extensão oficial da **Microsoft** e selecione **Instalar (Install)**.

---

## 3. Instalando o Python pelo Terminal

Com a extensão pronta, vamos instalar o interpretador do Python.

### Passo 1: Abrir o Terminal do VS Code
* Pressione `Ctrl + '` (ou vá no menu superior: `Terminal` > `Novo Terminal`).

### Passo 2: Executar o Comando de Instalação

Escolha o comando correto para o seu sistema:

* **Windows (PowerShell ou Command Prompt):**
  ```bash
  winget install Python.Python.3.12
  ```

* **macOS:**
  ```bash
  brew install python
  ```

* **Linux (Ubuntu / Debian):**
  ```bash
  sudo apt update && sudo apt install python3 -y
  ```

### Passo 3: Testar a Instalação
Feche o terminal, abra um novo terminal e digite:
```bash
python --version
```
*(Se aparecer algo como `Python 3.x.x`, a instalação foi um sucesso!)*

---

## 4. Seu Primeiro Código: "Hello World"

Na programação, existe uma tradição de que o primeiro código escrito em qualquer linguagem deve exibir a mensagem *"Hello, World!"* (Olá, Mundo!).

### Criando o arquivo:
1. No VS Code, crie um novo arquivo chamado `01_hello_world.py`.
2. Digite o seguinte código:

```python
# 01_hello_world.py

# A função print() exibe um texto na tela
print("Hello, World!")
print("Bem-vindo ao Curso de Python do Zero!")
```

### Como Executar no VS Code:
* **Opção 1:** Clique no botão de **Play (▶)** no canto superior direito do editor.
* **Opção 2:** No terminal do VS Code, digite:
  ```bash
  python 01_hello_world.py
  ```

---

## 5. Exercício Prático

Crie um arquivo chamado `exercicio_modulo1.py` na pasta `modulo_1/` e escreva um código que exiba três linhas no terminal:
1. Seu nome completo.
2. A sua cidade/estado.
3. A frase: *"Estou aprendendo Python no VS Code!"*.

---

### 🟢 Próximo Passo
Após concluir os testes do Módulo 1, avançaremos para o **Módulo 2: Variáveis e Tipos de Dados**!

---

## 🔗 **Como Contribuir / Contato**</br></br>
Este projeto foi desenvolvido como parte de um desafio prático de segurança cibernética. Sinta-se à vontade para explorá-lo, cloná-lo e adaptá-lo!

| Botão | Ação |
| :--- | :--- |
| ⭐ Dar Estrela | Se gostou do projeto, considere dar uma estrela no GitHub. |
| 🤝 Conecte-se | **<img src="https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Link para o LinkedIn" align="center"> <a href="https://www.linkedin.com/in/leandro-antonio-fortunato/" target="_blank">  Visite meu linkedin</a>**  |
| 📧 Fale Comigo | 📧 [E-mail para contato](mailto:leandroantonio.fortunato@hotmail.com) |
