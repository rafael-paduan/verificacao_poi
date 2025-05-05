# Verificação de POIs com Google Maps

Este projeto realiza a verificação de Pontos de Interesse (POIs) utilizando a API do Google Maps, a partir de um arquivo CSV de entrada com dados de unidades (nome, endereço, coordenadas, etc). O notebook executa geocodificação de endereços, busca POIs próximos e gera um relatório final consolidado.

## Funcionalidades

- Geocodificação de endereços usando Google Geocoding API
- Busca de POIs próximos por bandeira e nome da unidade usando Google Places API
- Cálculo de distância entre coordenadas
- Geração do CSV final com informações dos POIs encontrados

## Requisitos

- Python 3.9+
- Conta e chave de API do Google Maps com acesso às APIs Geocoding e Places

## Instalação

Instale as dependências com:

```sh
pip install -r requirements.txt
```

## Como usar

1. Edite o notebook `verificacao_poi.ipynb` e configure:
   - `GOOGLE_API_KEY` com sua chave da API Google
   - `INPUT_FILE` com o caminho do seu arquivo CSV de entrada
   - `FINAL_OUTPUT_FILE` com o caminho desejado para o arquivo de saída

2. Execute o notebook célula por célula no Jupyter ou VS Code.

3. O resultado será salvo no arquivo definido em `FINAL_OUTPUT_FILE`.

## Observações

- O notebook faz requisições à API do Google, podendo consumir créditos da sua conta Google Cloud.
- O arquivo de entrada deve conter colunas como `bandeira`, `nome_unidade`, `logradouro`/`endereco`, `municipio`/`cidade` e/ou coordenadas (`latitude`, `longitude`).
