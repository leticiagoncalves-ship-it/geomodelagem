# Trabalho de GeoModelagem e Visão Computacional - Açaí e Barbeiro

Este repositório contém o desenvolvimento prático da análise integrada da produção de açaí no Estado do Pará, combinando geoprocessamento, dados meteorológicos, modelagem espacial e visão computacional.

## 🎓 Informações Acadêmicas
* **Instituição:** Universidade Estadual do Norte Fluminense Darcy Ribeiro (UENF)
* **Laboratório:** LAMET - Laboratório de Meteorologia
* **Programa:** Mestrado em Clima e Energia
* **Disciplina:** GeoModelagem do Potencial Energético e do Microclima Urbano
* **Professora:** Dra. Raquel Jahara Lobosco
* **Desenvolvido em Dupla por:** * Letícia Raquel Trindade Gonçalves
  * Rafael de Oliveira Menezes

---

## 🗺️ Parte 1 – Mapeamento Climático
Nesta etapa, criamos os mapas climáticos sazonais do Estado do Pará utilizando a biblioteca `Cartopy` em Python, destacando a principal região produtora de açaí (Igarapé-Miri, Cametá, Abaetetuba e entorno). 
Foram processados dados meteorológicos da base Copernicus (`ERA5`/`ERA5-Land`) referentes ao ano de 2024 (horário das 15h) para produzir os 16 mapas climáticos cobrindo as quatro estações para as variáveis de:
* Precipitação
* Temperatura do Ar (convertida de Kelvin para Celsius)
* Intensidade do Vento ($V = \sqrt{u^2 + v^2}$)
* Umidade Específica

## 👁️ Parte 2 – Visão Computacional com YOLO
Aplicação de visão computacional utilizando a biblioteca `YOLO/Ultralytics` para detectar elementos associados à produção de açaí e ao risco sanitário. O modelo foi treinado para realizar a detecção visual do inseto vetor (*barbeiro/triatomíneo*) e das estruturas do fruto (*acai*, *cacho*).

---

## 📊 Parte 3 – Análise Integrada entre Clima e Produção de Açaí

Abaixo apresenta-se a tabela comparativa e o gráfico correlacionando os dados meteorológicos do Copernicus com os aspectos ecológicos e biológicos observados na região produtora de Igarapé-Miri, Abaetetuba e Cametá.

### 📈 Tabela Comparativa Sazonal

| Estação | Precipitação | Temperatura | Umidade | Vento | Índice de Produção de Açaí |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Verão** *(Dez-Fev)* | Moderada (~250 mm) | Alta (~28.5 °C) | Alta (~0.016 kg/kg) | Moderado (~3.0 m/s) | **Baixo** *(Entresafra)* |
| **Outono** *(Mar-Mai)* | **Muito Alta** (~420 mm) | Amena (~26.5 °C) | **Máxima** (~0.018 kg/kg) | Fraco (~2.0 m/s) | **Baixo** *(Frutos em formação)* |
| **Inverno** *(Jun-Ago)* | Baixa (~100 mm) | Alta (~29.0 °C) | Moderada (~0.0145 kg/kg) | Forte (~4.0 m/s) | **Alto** *(Início da colheita)* |
| **Primavera** *(Set-Nov)* | **Mínima** (~50 mm) | **Máxima** (~32.0 °C) | **Mínima** (~0.0135 kg/kg) | **Muito Forte** (~5.0 m/s) | **Muito Alto** *(Pico da safra)* |

### 📉 Gráfico de Correlação Sazonal

![Gráfico de Análise Integrada](resultados/grafico_analise_integrada.png)
