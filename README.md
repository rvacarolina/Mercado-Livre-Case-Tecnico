# Mercado Livre - Case Técnico

Neste repositório consta a solução dos três problemas propostos pelo Case Técnico. O nome dos arquivos condiz com o problema, por exemplo: parte1.ipynb é o código referente ao primeiro problema.\
Também existe o 'xgb_model.pickle', o qual se refere ao modelo criado em parte3.ipynb.\
Os dados estão na pasta 'Teste Técnico - DS'.

## Requisitos

O projeto foi desenvolvido com Python 3.8.8 através do Anaconda. As bibliotecas necessárias para executar o código estão dentro de requirements.txt e deposem ser instaladas através do seguinte comando:

```
pip install -r /path/to/requirements.txt
```

É necessário que você tenha o Python instalado localmente. Caso não tenha, instale através deste [link](https://www.python.org/).

## Como executar

Para executar o código, basta abrir um dos códigos e executar em um editor que suporte o formato Jupyter Notebook (.ipynb).\
Caso queira testar o modelo existentes com novos dados, basta executar o código abaixo.

```python
import pandas as pd
import pickle

#Carregando o modelo
model=pickle.load(open('model.pkl','rb'))

#Exemplo - Lendo novos dados
df = pd.read_csv('test.csv')
predictions=model.predict(df)
print(predictions)

```
