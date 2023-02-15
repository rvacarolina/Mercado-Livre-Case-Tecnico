# Incognia - Payments Chargeback Prediction

A base de dados Payments apresenta eventos de transações por meio de diferentes
variáveis, como valor da transação e a região geográfica em que ela foi realizada.
Adicionalmente, existe a coluna chargedback que indica se a transação ocasionou um
chargeback.
Neste contexto, o objetivo é construir um modelo para predizer corretamente os casos de chargeback através das variáveis disponíveis na base de dados.

## Requisitos

O projeto foi desenvolvido com Python 3.8.8 através do Anaconda. As bibliotecas necessárias para executar o código estão dentro de requirements.txt e deposem ser instaladas através do seguinte comando:

```
pip install -r /path/to/requirements.txt
```

É necessário que você tenha o Python instalado localmente. Caso não tenha, instale através deste [link](https://www.python.org/).

## Estrutura do diretório

├── images                                    # Imagens geradas pelo código
├── incognia-cin-data                   # Dados
├── pickle                                      # Modelos salvos
├... code.ipynb                                #Código em Jupyter Notebook
├... code.py                                     #Código em Python
├... requirements.txt                        #Bibliotecas do Python
├... Relatório - Carolina Robledo Velini de Andrade.pdf               #Relatório

└... README.md

## Como executar

Para executar o código completo, basta abrir e executar em um editor de código com Python um arquivo de sua preferência (code.ipynb ou code.py).
Caso queira testar um dos modelos existentes com novos dados, basta executar o código abaixo.

```python
import pandas as pd

#Carregando o modelo
model=pickle.load(open('model.pkl','rb'))

#Exemplo - Lendo novos dados em parquet
df = pd.read_parquet('test.parquet')
predictions=model.predict(df)
print(predictions)

```
