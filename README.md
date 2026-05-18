# Chat-Bot-Gabriel-
# README — Projeto GOB ChatBot com LangChain + Groq

## 📌 Contexto do Projeto

O projeto **GOB (Gerador de Orientações Básicas)** foi desenvolvido como um primeiro assistente virtual utilizando **Python**, **LangChain** e a API da **Groq**, com o objetivo de criar uma aplicação simples de conversação em terminal.
Foi feito no Google colab

A proposta do sistema é demonstrar, de forma prática, como integrar modelos de linguagem (LLMs) em aplicações Python, permitindo interações inteligentes entre usuário e assistente virtual.

---

# 🎯 Objetivo do Projeto

O principal objetivo deste projeto é:

* Criar um chatbot funcional utilizando modelos de IA generativa;
* Utilizar o framework LangChain para gerenciamento de prompts;
* Simular uma conversa natural entre usuário e inteligência artificial;
* Servir como base para futuros projetos mais avançados de assistentes virtuais.

---

# 👀 Visão Geral da Solução

A aplicação funciona via terminal (CLI — Command Line Interface), onde o usuário envia perguntas e o chatbot responde utilizando o modelo:

* `llama-3.3-70b-versatile`

---

# 🏗️ Arquitetura da Solução

## Componentes Utilizados

### 1. Python

Responsável pela estrutura principal da aplicação.

### 2. LangChain

Framework utilizado para:

* Gerenciamento de prompts;
* Encadeamento de chamadas;
* Organização do histórico da conversa.

### 3. Groq API

Responsável pela execução do modelo de linguagem.

### 4. Modelo LLM

Modelo utilizado:

```python
llama-3.3-70b-versatile
```

---

# ⚙️ Fluxo de Funcionamento

```text
Usuário
   ↓
Input da Mensagem
   ↓
Histórico de Conversa
   ↓
ChatPromptTemplate (LangChain)
   ↓
Modelo LLM via Groq
   ↓
Resposta Gerada
   ↓
Exibição no Terminal
```

---

# 🧠 Explicação do Código

## Importação das Bibliotecas

```python
import os
from langchain_core.prompts import ChatPromptTemplate
from langchain_groq import ChatGroq
```

As bibliotecas são utilizadas para:

* Manipulação de variáveis de ambiente;
* Criação dos prompts;
* Comunicação com a API da Groq.

---

## Configuração da API Key

```python
api_key = 'sua api'
os.environ['GROQ_API_KEY'] = api_key
```

Define a chave de autenticação da API da Groq.

---

## Inicialização do Modelo

```python
chat = ChatGroq(model='llama-3.3-70b-versatile')
```

Seleciona o modelo de IA utilizado pelo chatbot.

---

## Função Principal do Bot

```python
def resposta_bot(mensagens):
```

Responsável por:

* Montar o histórico da conversa;
* Criar o template de mensagens;
* Enviar para o modelo;
* Retornar a resposta da IA.

---

## Loop de Conversação

```python
while True:
```

Mantém a aplicação em execução até o usuário digitar:

```text
x
```
---

## 2. Instale as Dependências

```bash
pip install langchain
pip install langchain-groq
```

---

## 3. Configure sua API Key

No código:

```python
api_key = 'SUA_API_KEY'
```

Substitua pela sua chave válida da Groq.

* Para criar sua chave:
* Primeiro: Entre no site da groq api keys; link: https://console.groq.com/keys
* Segundo: Crie uma conta no groq;
* Terceiro: Crie uma chave de API;
* Quarto: Copie essa chave e coloque no local do código 'SUA_API_KEY'.

---

## 4. Interaja com o Chatbot

Exemplo:

```text
Usuário: Olá
Bot: Olá! Como posso ajudar você hoje?
```

Para finalizar:

```text
Usuário: x
```
---

---

# 📖 Conclusão

O projeto GOB demonstra de forma prática como construir um chatbot utilizando modelos modernos de inteligência artificial com Python e LangChain.

Além de servir como aprendizado sobre integração com LLMs, o projeto também estabelece uma base sólida para evolução futura em aplicações de IA conversacional.

---

# 👨‍💻 Autor

Projeto desenvolvido para estudos e aprendizado em Inteligência Artificial e desenvolvimento de chatbots com Python.
