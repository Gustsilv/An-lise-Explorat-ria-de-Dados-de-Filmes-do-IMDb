# Análise Exploratória de Dados de Filmes do IMDb

---

## 📄 Descrição do Projeto

Este projeto tem como objetivo realizar a coleta de dados (web scraping) de informações de filmes do site [IMDb (Internet Movie Database)](https://www.imdb.com/), utilizando a biblioteca **Selenium** em Python. Após a coleta, os dados são organizados, limpos e submetidos a uma **Análise Exploratória de Dados (EDA)** com as bibliotecas **Pandas**, **NumPy**, **Matplotlib** e **Seaborn**.

O propósito é extrair insights sobre filmes, como sua distribuição de avaliações, popularidade ao longo dos anos, e a relação entre o ano de lançamento e a avaliação média.

## 🚀 Tecnologias Utilizadas

* **Python:** Linguagem de programação principal.
* **Selenium:** Para web scraping e automação de navegador.
* **Pandas:** Para manipulação e análise de dados.
* **NumPy:** Para operações numéricas de alto desempenho.
* **Matplotlib:** Para criação de gráficos estáticos.
* **Seaborn:** Para visualizações estatísticas mais atraentes.

## ⚙️ Como Executar o Projeto

Siga os passos abaixo para configurar e rodar o projeto em sua máquina local:

### Pré-requisitos

Certifique-se de ter o **Python** (preferencialmente via [Anaconda](https://www.anaconda.com/download)) instalado.

Você também precisará do **ChromeDriver** compatível com a versão do seu navegador Google Chrome.
1.  Verifique a versão do seu Chrome (Ajustes > Ajuda > Sobre o Google Chrome).
2.  Baixe o ChromeDriver correspondente em [https://chromedriver.chromium.org/downloads](https://chromedriver.chromium.org/downloads).
3.  Descompacte o arquivo e coloque o executável `chromedriver.exe` (ou `chromedriver` em macOS/Linux) em uma pasta chamada `drivers` na raiz do seu projeto.

Exemplo de estrutura de pasta:
```
seu_projeto_imdb/
├── drivers/
│   └── chromedriver.exe  (ou chromedriver)
└── imdb_scraper.py
```

### Instalação das Dependências

Abra o terminal (ou **Anaconda Prompt** se estiver usando Anaconda) na pasta raiz do projeto e execute o comando:

```bash
pip install selenium pandas numpy matplotlib seaborn
```
### Execução do Script
Após instalar as dependências e configurar o ChromeDriver, execute o script Python:

```Bash

python imdb_scraper.py
```
O script irá:
1. Abrir uma janela do navegador Chrome.
2. Navegar até a página do IMDb configurada para coleta de dados.
3. Coletar informações de filmes (Título, Ano, Avaliação).
4. Processar e limpar os dados com Pandas.
5. Gerar e exibir gráficos de análise exploratória de dados.

## 📊 Análise e Visualizações
Nesta etapa, o script realiza:
- Estatísticas Descritivas: df.info() e df.describe() para um panorama dos dados.
- Distribuição das Avaliações: Histograma com KDE para entender a frequência das avaliações.
- Filmes por Ano de Lançamento: Gráfico de barras mostrando a contagem de filmes por ano.
- Avaliação Média por Ano: Gráfico de linha para visualizar a tendência da avaliação média ao longo do tempo.
- Dispersão Ano vs. Avaliação: Gráfico de dispersão para identificar relações entre o ano e a avaliação individual.

## 🚧 Desafios e Próximos Passos
Durante o desenvolvimento, foi identificado que a página inicial de web scraping (/chart/moviemeter/) focava em filmes muito recentes, limitando a análise histórica. Para superar isso, o próximo passo será ajustar o web scraping para coletar dados da página IMDb Top 250 Filmes (https://www.imdb.com/chart/top/), que oferece uma amostra de filmes mais diversificada em termos de ano de lançamento.

Ajustes nos seletores CSS/XPath serão necessários para se adequar à nova estrutura da página.

## 🤝 Contribuições
Contribuições são bem-vindas! Se tiver sugestões ou melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## 📝 Licença
Este projeto está licenciado sob a Licença MIT.
