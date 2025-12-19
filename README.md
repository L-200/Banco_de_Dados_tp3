# 📊 Estudo de Transações e Concorrência em Banco de Dados (TP3)

Trabalho prático focado na análise de desempenho, controle de concorrência e transações (ACID) em ambientes relacionais.

---

## 👥 Autores

* **Lucas de Souza Cerveira Pereira**
* **Mikaelle Costa de Santana**
* **Roberta Graziela de Oliveira Brasil**

---

## 📝 Sobre o Projeto

Este repositório contém o **Trabalho Prático 3 (TP3)**, cujo objetivo principal é a familiarização prática com conceitos avançados de Sistemas de Gerenciamento de Banco de Dados (SGBD).

O notebook guia o usuário através de experimentos que demonstram:
1.  **Manipulação de Dados:** Uso de SQL integrado ao Python (via `pandas` e `sqlalchemy`).
2.  **Gerenciamento de Transações:** Simulação de cenários de escrita concorrente (ex: reserva de assentos).
3.  **Níveis de Isolamento:** Comparação entre *Read Committed* e *Serializable*.
4.  **Condições de Corrida:** Análise de falhas lógicas em sistemas concorrentes e estratégias de mitigação (Bloqueio Otimista vs. Pessimista).

---

## ⚙️ Pré-requisitos de Ambiente

Para executar os experimentos, é necessário ter um servidor **PostgreSQL** rodando localmente.

### Configuração do Banco de Dados
O notebook assume a existência de um usuário e banco de dados específicos para conexão. Certifique-se de que seu PostgreSQL possua:

* **Usuário:** `icomp`
* **Senha:** `icomp123`
* **Database:** `icomp`
* **Permissões:** O usuário não precisa ser superusuário, mas deve ter permissão de leitura/escrita no banco `icomp`.

> **Nota:** Essa configuração foi padronizada para atender aos critérios de avaliação da disciplina.

---

## 🚀 Instalação e Execução

Siga os passos abaixo para configurar o ambiente virtual e conectar o Jupyter Kernel corretamente.

### 1. Preparar o Ambiente Virtual (`venv`)

Abra o terminal na raiz do projeto e execute:

```bash
# 1. Crie o ambiente virtual
python3 -m venv .venv

# 2. Ative o ambiente
source .venv/bin/activate
```

### 2. Instalar Dependências

Instale as bibliotecas necessárias (Jupyter, drivers de banco e análise de dados):

```bash
# Instala o suporte ao Kernel do Jupyter
pip install ipykernel

# Instala as bibliotecas usadas no notebook (pandas, psycopg2, sqlalchemy, etc)
pip install pandas psycopg2-binary sqlalchemy ipython-sql matplotlib
```

### 3. Registrar o Kernel

Para que o Jupyter reconheça este ambiente virtual específico, registre-o:

```bash
python -m ipykernel install --user --name tp3 --display-name "Python (TP3)"
```

### 4. Rodar o Notebook

1. Abra o Jupyter Notebook ou Jupyter Lab.

2. Abra o arquivo Notebook_tp3.ipynb.

3. No menu superior, vá em Kernel -> Change Kernel e selecione Python (TP3).

4. Execute as células sequencialmente.

## 🧪 Resumo dos Experimentos

O trabalho conclui com uma análise de trade-offs em engenharia de dados, demonstrando que:

- Consistência Estrita (Serializable): Garante a integridade, mas custa caro em performance devido a retries e coordenação.

- Estratégias Otimistas: Em níveis de isolamento menores (como Read Committed), validar o dado antes da escrita (ex: WHERE disp = TRUE) oferece melhor vazão (throughput) para sistemas de alta concorrência.

## ⚖️ Licença

Este projeto foi desenvolvido para fins acadêmicos. Sinta-se a vontade para forká-lo, estudá-lo e utilizá-lo como preferir.