# An-lise-de-Qualidade-de-Dados-com-PySpark-e-PyDeequ-no-Google-Colab

# PySpark and PyDeequ Data Quality Checks - README

"""
Este é um projeto que utiliza o PySpark e o PyDeequ para realizar verificações de qualidade de dados em um ambiente Google Colab.

## Requisitos

- Python 3.x
- PySpark 3.0.3
- NGROK (para exposição externa do SparkUI no Google Colab)
- PyDeequ

## Configuração do Ambiente no Google Colab

# Instalar PySpark
!pip install pyspark==3.0.3

# Instalar NGROK
!wget -qnc https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
!unzip -n -q ngrok-stable-linux-amd64.zip

# Autenticar a sessão do SparkUI com NGROK
!./ngrok authtoken YOUR_NGROK_AUTH_TOKEN
get_ipython().system_raw('./ngrok http 4050 &')
!sleep 10
!curl -s http://localhost:4040/api/tunnels | grep -Po 'public_url":"(?=https)\K[^"]*'

# Montar o Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Instalar PyDeequ
!pip install pydeequ

## Executando a Análise

# Carregar o notebook principal
from google.colab import files
uploaded = files.upload()

# Estrutura do Projeto
- analyze_data.ipynb: Notebook principal para execução da análise.
- drive/MyDrive/Colab Notebooks/case_final.json: Arquivo de dados de exemplo (substitua pelo seu p
