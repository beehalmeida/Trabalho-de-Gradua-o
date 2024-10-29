import pandas as pd
# Loop para ler cada arquivo e converter em dataframe
from google.colab import drive
drive.mount ('/content/drive')
path_in = '/content/drive/My Drive/PYTHON/Dados Cargas'
df = pd.read_csv(path_in + "/2015Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df2 = pd.read_csv(path_in + "/2016Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df3 = pd.read_csv(path_in + "/2017Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df4 = pd.read_csv(path_in + "/2018Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df5 = pd.read_csv(path_in + "/2019Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df6 = pd.read_csv(path_in + "/2020Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df7 = pd.read_csv(path_in + "/2021Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df8 = pd.read_csv(path_in + "/2022Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
df9 = pd.read_csv(path_in + "/2023Carga.txt", low_memory=False, sep=";", encoding="UTF-8", decimal=",")
# Verificando as primeiras linhas do dataframe final
df.head(5)
# listando o dataframe
dataframes = [df, df2, df3, df4, df5, df6, df7, df8, df9]  
# Concatenando os DataFrames em um único DataFrame
dataframe_final_cargas = pd.concat(dataframes, ignore_index=True)
# Salvando o dataframe final em um arquivo csv
dataframe_final_cargas.to_csv('/content/drive/My Drive/PYTHON/Dados Cargas/dataframe_final_cargas.csv',index=False)
