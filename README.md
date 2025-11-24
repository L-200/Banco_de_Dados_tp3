# Instruções para rodar

1) Crie o venv localmente pelo terminal 

```bash
python3 -m venv .venv
```

2) Ative o venv

```bash 
source .venv/bin/activate
```

3) Instalar o ipykernel

```bash 
pip install ipykernel
```

4) Registrar o kernel dentro do ambiente 

```bash
python -m ipykernel install --user --name tp3 --display-name "Python (TP3)"
```

5) Após isso utilize a opção venv para kernel de execução das células