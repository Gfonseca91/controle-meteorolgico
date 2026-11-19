```markdown
# 🌍 Monitor de Temperatura Global via Planilha e API

![Python](https://img.shields.io/badge/python-3578E5?style=for-the-badge&logo=python&logoColor=white) 
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) 
![Requests](https://img.shields.io/badge/requests-000000?style=for-the-badge&logo=python&logoColor=white)
![Open-Meteo](https://img.shields.io/badge/API-Open--Meteo-blue?style=for-the-badge)

Este projeto automatiza a coleta de dados de coordenadas geográficas armazenadas em uma **Google Planilha** e consulta em tempo real a temperatura atual de cada localidade utilizando a **API Open-Meteo**.

---

## 🚀 Funcionalidades

- **Integração Direta**: Lê dados dinamicamente de uma planilha pública do Google Sheets convertida em formato CSV.
- **Geolocalização & Clima**: Utiliza as coordenadas de latitude e longitude de cada registro para buscar a temperatura atual.
- **Escalabilidade**: Estrutura pronta para iterar sobre múltiplos registros de forma automatizada.

---

## 🛠️ Tecnologias Utilizadas

* **[Python](https://www.python.org/)** — Linguagem base do projeto.
* **[Pandas](https://pandas.pydata.org/)** — Para manipulação e leitura ágil dos dados da planilha.
* **[Requests](https://requests.readthedocs.io/)** — Para requisições HTTP eficientes à API de clima.
* **[Open-Meteo API](https://open-meteo.com/)** — API pública e gratuita para dados meteorológicos precisos.

---

## 📊 Estrutura do Fluxo de Dados

1. **Leitura dos Dados**: O script acessa a URL de exportação da Google Planilha e carrega o DataFrame usando o `pandas`.
2. **Iteração**: Para cada linha (local cadastrado), o algoritmo extrai as coordenadas (`Latitude` e `Longitude`).
3. **Requisição à API**: O pacote `requests` envia os parâmetros para o endpoint da Open-Meteo solicitando o campo `current.temperature_2m`.
4. **Exibição**: O retorno JSON com os dados climáticos é exibido dinamicamente.

---

## 📋 Pré-requisitos

Caso queira rodar este projeto localmente, instale as dependências necessárias:

```bash
pip install pandas requests
```

---

## 🧑‍💻 Autoria e Contribuição

Sinta-se à vontade para clonar, sugerir melhorias ou aplicar novas features como visualizações gráficas de temperatura ou salvamento automático de relatórios em PDF/Excel!
```
