# 🎟️ Sistema de Gerenciamento de Senhas

Aplicação desktop desenvolvida com **Python** e **Tkinter** para geração, organização e chamada de senhas de atendimento.

O sistema possui uma tela para o cliente retirar sua senha, uma área administrativa para acompanhar a fila e um painel para exibir a senha chamada.

## 📖 Sobre o Projeto

Este projeto representa um sistema simples de gerenciamento de filas de atendimento.

Ao clicar no botão de geração, o cliente recebe uma senha sequencial no formato:

```text
A001
A002
A003
```

A senha é adicionada à fila e exibida na tela administrativa.

O atendente pode chamar a próxima senha da fila. Quando isso acontece, a senha é removida da lista de espera e apresentada no painel principal.

## 🎯 Objetivos

Este projeto foi desenvolvido com os seguintes objetivos:

* Praticar lógica de programação em Python;
* Criar interfaces gráficas com Tkinter;
* Trabalhar com múltiplas janelas;
* Gerar senhas sequenciais;
* Utilizar listas como filas;
* Inserir e remover elementos;
* Trabalhar com eventos de botões;
* Utilizar variáveis globais;
* Atualizar informações dinamicamente;
* Exibir mensagens ao usuário;
* Compreender o funcionamento de uma fila FIFO.

## ✨ Funcionalidades

O sistema possui:

* Geração automática de senhas;
* Numeração sequencial;
* Formatação com três dígitos;
* Inclusão das senhas em uma fila;
* Exibição da fila para o administrador;
* Chamada da próxima senha;
* Remoção da senha atendida;
* Painel com a senha atual;
* Aviso quando a fila está vazia;
* Mensagem informando a senha gerada;
* Três janelas integradas.

## 🖥️ Janelas do Sistema

### 👤 Tela do Cliente

A tela do cliente permite gerar uma nova senha de atendimento.

Ao clicar no botão **Gerar Senha**, o sistema:

1. Cria uma nova senha;
2. Adiciona a senha à fila;
3. Atualiza a lista administrativa;
4. Exibe uma mensagem com a senha;
5. Incrementa o contador.

### 🧑‍💼 Tela do Administrador

A tela administrativa apresenta:

* Lista de senhas aguardando;
* Botão para chamar a próxima senha.

As senhas são exibidas em um componente `Listbox`.

### 📺 Painel de Senhas

O painel apresenta a senha atual em tamanho destacado.

Inicialmente, o painel mostra:

```text
---
```

Quando uma senha é chamada, o valor é atualizado automaticamente.

## 🔢 Formato das Senhas

As senhas são geradas utilizando:

```python
senha = f"A{contador:03}"
```

O trecho `:03` garante que o número seja exibido com três dígitos.

Exemplos:

```text
1   → A001
12  → A012
100 → A100
```

## 📚 Funcionamento da Fila

As senhas são adicionadas ao final da lista:

```python
fila.append(senha)
```

A próxima senha é removida da primeira posição:

```python
senha = fila.pop(0)
```

Esse comportamento representa uma fila do tipo **FIFO**:

```text
First In, First Out
```

Ou seja, a primeira senha gerada é a primeira a ser atendida.

## 🔄 Fluxo da Aplicação

```text
Cliente solicita uma senha
            ↓
O sistema gera A001
            ↓
A senha entra na fila
            ↓
A senha aparece no painel administrativo
            ↓
O atendente chama a próxima senha
            ↓
A primeira senha é removida da fila
            ↓
A senha aparece no painel de atendimento
```

## 🛠️ Tecnologias Utilizadas

* Python;
* Tkinter;
* Visual Studio Code;
* Git;
* GitHub.

## 🧩 Componentes do Tkinter Utilizados

Durante o desenvolvimento foram utilizados:

* `Tk`;
* `Toplevel`;
* `Label`;
* `Button`;
* `Listbox`;
* `StringVar`;
* `messagebox`;
* `pack`;
* `mainloop`;
* `END`.

## 📂 Estrutura do Projeto

```text
python-sistema-gerenciamento-senhas/
├── index.py
└── README.md
```

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/ewertonmartinslopes/python-sistema-gerenciamento-senhas.git
```

### 2. Acesse a pasta

```bash
cd python-sistema-gerenciamento-senhas
```

### 3. Verifique a instalação do Python

```bash
python --version
```

### 4. Execute o programa

```bash
python index.py
```

Em alguns sistemas, utilize:

```bash
python3 index.py
```

O Tkinter normalmente acompanha a instalação padrão do Python.

## 📚 Conceitos Praticados

Durante o desenvolvimento foram utilizados:

* Importação de módulos;
* Interface gráfica;
* Múltiplas janelas;
* Variáveis;
* Variáveis globais;
* Funções;
* Eventos;
* Listas;
* Filas;
* Métodos `append()` e `pop()`;
* Estruturas condicionais;
* Contadores;
* F-strings;
* Formatação numérica;
* Atualização de componentes;
* Mensagens informativas;
* Mensagens de aviso.

## 💡 Aprendizados

Este projeto permitiu compreender como criar uma aplicação desktop com múltiplas janelas utilizando Tkinter.

Também foi possível praticar o conceito de fila, no qual as senhas são atendidas na ordem em que foram geradas.

A aplicação demonstra como integrar lógica de programação, estruturas de dados e elementos visuais em um sistema interativo.

## ⚠️ Limitações Atuais

As informações ficam armazenadas somente enquanto o programa está aberto.

Quando a aplicação é encerrada:

* A fila é apagada;
* O contador volta para 1;
* O histórico de atendimento é perdido.

Para um sistema real, seria necessário utilizar um banco de dados ou arquivo para persistência.

## 🔮 Melhorias Futuras

O projeto poderá receber:

* Senhas normais e prioritárias;
* Diferentes tipos de atendimento;
* Número do guichê;
* Histórico de senhas chamadas;
* Repetição da última senha;
* Botão para cancelar senha;
* Botão para reiniciar fila;
* Data e hora de emissão;
* Efeito sonoro na chamada;
* Voz anunciando a senha;
* Interface mais moderna;
* Tela cheia para o painel;
* Banco de dados;
* Relatórios de atendimento;
* Tempo médio de espera;
* Login administrativo;
* Geração de comprovante;
* Integração com impressora térmica;
* Geração de executável.

## 📌 Finalidade

Este projeto foi desenvolvido como parte das atividades do curso **Técnico em Desenvolvimento de Sistemas**.

O repositório integra meu portfólio e registra minha evolução em Python, interfaces gráficas, estruturas de dados e desenvolvimento de aplicações desktop.

## 👨‍💻 Autor

**Ewerton Martins Lopes**

Estudante do curso Técnico em Desenvolvimento de Sistemas e desenvolvedor Full Stack em formação.
