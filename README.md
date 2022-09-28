# Indicadores Economicos-Jupyter
Como utilizar la API de indicadores.cl con Jupyter Notebook/Lab y Pandas.

# Inicio Rapido

```
#Importar librerias
import requests
import pandas as pd

#Definir la url
url_uf = 'https://mindicador.cl/api/uf'

#Realiza un GET para traer la informacion
r = requests.get(url_uf)

#Transforma los datos a formato JSON
j = r.json()

#Transforma la informacion de formato JSON a Tabla con Pandas
df = pd.DataFrame(j['serie'])

#Imprimir la tabla
df
```
|	 |fecha	| valor |
| --- | --- | --- |
|0	|2022-09-27T03:00:00.000Z	|34217.38|
|1	|2022-09-26T03:00:00.000Z	|34203.78|
|2	|2022-09-25T03:00:00.000Z	|34190.18|
|3	|2022-09-24T03:00:00.000Z	|34176.59|
|4	|2022-09-23T03:00:00.000Z	|34163.01|
...
|30	|2022-08-28T04:00:00.000Z	|33791.01|
