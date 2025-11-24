# Sobre este trabalho

O Notebook segue uma série de instruções presentes no pdf. 

O propósito geral do trabalho é a familiarização com SQL, transações, índices e otimizadores.

# Pré-requisitos para o funcionamento do notebook:

É assumido que já existe um usuário icomp, de senha icomp123 e com um banco de dados icomp rodando no postgres da sua máquina. O usuário não precisa ser superusário.

Esses pré-requisitos são necessários pois era só isso que tivemos acesso para usar na avaliação do trabalho.

# Instruções para rodar

1) Crie o venv localmente pelo terminal 

```bash
python3 -m venv .venv
```

2) Ative o venv

```bash 
source .venv/bin/activate
```

3) Instale o ipykernel

```bash 
pip install ipykernel
```

4) Registre o kernel dentro do ambiente 

```bash
python -m ipykernel install --user --name tp3 --display-name "Python (TP3)"
```

5) Após isso utilize a opção venv para kernel de execução das células