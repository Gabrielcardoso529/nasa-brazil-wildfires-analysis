# Dados do projeto

Este projeto utiliza dados de focos de calor/incêndio obtidos por meio da plataforma NASA FIRMS (Fire Information for Resource Management System).

## Arquivo utilizado

O notebook original foi desenvolvido com o arquivo:

`fire_archive_SV-C2_755280.csv`

A base analisada contém 853.047 registros referentes ao Brasil no período de 25/05/2025 a 25/05/2026.

## Como preparar os dados

1. Acesse a plataforma NASA FIRMS/Earthdata e obtenha os dados correspondentes ao recorte utilizado na análise.
2. Salve o arquivo CSV nesta pasta com o nome `fire_archive_SV-C2_755280.csv`.
3. Abra `notebooks/nasa_wildfires_analysis.ipynb` e execute as células em sequência. O notebook procura o CSV tanto a partir da raiz do repositório quanto da pasta `notebooks/`.

## Por que o CSV não está no GitHub?

O arquivo original possui aproximadamente 68 MB. Para manter o repositório leve e evitar versionar uma base de dados grande, o CSV não é armazenado diretamente aqui.

## Fonte

NASA FIRMS — Fire Information for Resource Management System / NASA Earthdata.

> A disponibilidade, o formato e os procedimentos de download dos dados podem mudar ao longo do tempo. Consulte a documentação oficial da NASA FIRMS para obter os dados.
