# Projeto Final - Pipeline ETL com PokeAPI

## Descrição

Este projeto é uma implementação de um pipeline ETL (Extração, Transformação e Carga) usando a PokeAPI. O objetivo do projeto é extrair dados de pokémons, habilidades e linguagens da PokeAPI, transformar os dados conforme necessário e carregá-los em um banco de dados SQLite para posterior consulta. Além disso, o projeto inclui um sistema de alerta para notificar falhas no processo de extração.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

projeto_final_etl_coderhouse/
│
├── notebooks/
│ ├── etl_pipeline.ipynb # Notebook Jupyter com a implementação do pipeline ETL
│
├── src/
│ ├── extract.py # Script para extração de dados
│ ├── load.py # Script para carga de dados no banco de dados
│ ├── transform.py # Script para transformação de dados
│
└── README.md # Este arquivo README

## Funcionalidades

- **Extração:** Os dados são extraídos de três endpoints da PokeAPI (`/pokemon`, `/ability`, `/language`).
- **Transformação:** Os dados são transformados em dataframes pandas.
- **Carga:** Os dados transformados são carregados em um banco de dados SQLite.
- **Alertas:** Um sistema de alerta notifica falhas no processo de extração utilizando a biblioteca `plyer`.

## Instalação

Para executar este projeto, siga as instruções abaixo:

1. Clone o repositório:

   ```sh
   git clone <https://github.com/matheusvazdata/projeto_final_etl_coderhouse.git>
   cd <projeto_final_etl_coderhouse>
   ```

2. Crie um ambiente virtual e ative-o:

   ```sh
   python -m venv venv
   source venv/bin/activate  # No Windows use: venv\Scripts\activate
   ```

3. Instale as dependências:
   ```sh
   pip install -r requirements.txt
   ```

## Uso

Para executar o pipeline ETL, abra e execute todas as células do notebook `notebooks/etl_pipeline.ipynb` em um ambiente Jupyter Notebook.

### Estrutura do Notebook

1. **Instalação das bibliotecas necessárias**
2. **Importação das bibliotecas**
3. **Definição da função de alerta**
4. **Definição da função para extrair dados da API**
5. **Definição da função para extrair dados detalhados dos Pokémons**
6. **Definição da função para extrair três tabelas da API e relacionar dados**
7. **Definição da função para carregar dados no banco de dados**
8. **Execução da extração, transformação e carga dos dados**
9. **Visualização dos dados extraídos**

## Exemplo de Saída

Abaixo estão as primeiras linhas dos dataframes carregados no banco de dados:

### Dados dos Pokémons

name | url
0 bulbasaur | https://pokeapi.co/api/v2/pokemon/1/
1 ivysaur | https://pokeapi.co/api/v2/pokemon/2/
2 venusaur | https://pokeapi.co/api/v2/pokemon/3/
3 charmander | https://pokeapi.co/api/v2/pokemon/4/
4 charmeleon | https://pokeapi.co/api/v2/pokemon/5/

### Dados das Habilidades

habilidade_1 | habilidade_2 | habilidade_3 | habilidade_4 | habilidade_5
0 overgrow | chlorophyll | None | None | None
1 overgrow | chlorophyll | None | None | None
2 overgrow | chlorophyll | None | None | None
3 blaze | solar-power | None | None | None
4 blaze | solar-power | None | None | None

### Dados das Linguagens

linguagem_1 | linguagem_2 | linguagem_3 | linguagem_4 | linguagem_5
0 English | Japanese | French | German | None
1 English | Japanese | French | German | None
2 English | Japanese | French | German | None
3 English | Japanese | French | German | None
4 English | Japanese | French | German | None

## Contribuição

Se você quiser contribuir com este projeto, sinta-se à vontade para fazer um fork do repositório, criar uma branch para suas alterações e abrir um pull request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
