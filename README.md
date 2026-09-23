# Sentinel-Time-Viewer

Comparação temporal de imagens Sentinel-2 utilizando controle deslizante (swipe) e sobreposição vetorial via Google Earth Engine e geemap.

## Visão Geral

Este notebook documenta e implementa uma interface interativa para visualização e comparação temporal de imagens de satélite Sentinel-2. O sistema é operado sobre a plataforma Google Earth Engine (GEE) e utiliza a biblioteca geemap em ambiente Google Colab. A aplicação viabiliza a comparação entre dois períodos anuais distintos por meio de um controle deslizante, garantindo a exibição contínua da delimitação vetorial da área de interesse em todas as camadas de visualização.

## Funcionalidades

* Upload direto de delimitações espaciais (formato Shapefile compactado em .zip) para o ambiente Colab;
* Filtragem automatizada de coleções Sentinel-2 com limite de cobertura de nuvens inferior a 10%;
* Seleção e renderização de composições de imagens agregadas por ano;
* Controle deslizante (swipe) interativo para análise de variação temporal;
* Renderização persistente do contorno do polígono vetorial sobreposto às camadas raster.

## Dados Utilizados

* **Base de Dados:** [Sentinel-2 Surface Reflectance](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR?utm_source=gemini)
* **Coleção GEE:** `COPERNICUS/S2_SR`
* **Composição de Bandas:** `B4` (Red), `B3` (Green), `B2` (Blue)

## Requisitos de Sistema

* Credenciais ativas e autenticadas no Google Earth Engine.
* Ambiente de execução Google Colab.
* Dependências da linguagem Python:
* `earthengine-api`
* `geemap`
* `ipywidgets`



## Instruções de Uso

1. Acesse o script interativo hospedado no repositório e inicie a execução no Google Colab clicando [aqui](https://github.com/samuel-c-santos/Sentinel-Time-Viewer/blob/main/GEE_swipe.ipynb?utm_source=gemini).
2. Realize o upload do arquivo vetorial delimitador (Shapefile em formato .zip).
3. Aguarde a centralização automática da visualização cartográfica na área de interesse e a inicialização da interface.
4. Defina os anos desejados nos menus correspondentes para o carregamento e renderização das respectivas coleções.
5. Utilize o controle deslizante para inspecionar a área, observando a variação da superfície sob o limite do polígono vetorial.

## Desenvolvimentos Futuros

* Integração com bases de dados dos sensores Landsat (LC08, LC09);
* Implementação de rotinas para cálculo e renderização de índices espectrais (e.g., NDVI, NBR);
* Rotinas de exportação das composições visuais processadas;
* Refinamento do filtro temporal para permitir análises sazonais ou semestrais.

## Demonstração

## Autoria

Samuel da Costa dos Santos

Especialista em Geoprocessamento | Regularização Ambiental | GEE & Python
