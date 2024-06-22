# Projeto Final - Pipeline ETL com PokeAPI

## Descrição

Este projeto é uma implementação de um pipeline ETL (Extração, Transformação e Carga) usando a PokeAPI. O objetivo do projeto é extrair dados de pokémons, habilidades e tipos de Pokémon da PokeAPI, transformar os dados conforme necessário e carregá-los em um banco de dados SQLite para posterior consulta. Além disso, o projeto inclui um sistema de alerta para notificar falhas no processo de extração.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

projeto_final_etl_coderhouse/ </br>
│ </br>
├── notebooks/ </br>
│ ├── etl_pipeline.ipynb </br>
│ </br>
├── venv/ # Ambiente virtual para gerenciamento de dependências </br>
│ ├── Include/ </br>
│ ├── Lib/ </br>
│ ├── Scripts/ </br>
│ ├── pyvenv.cfg </br>
│ </br>
├── pokeapi_data.db </br>
├── README.md </br>
├── requirements.txt </br>

## Funcionalidades

- **Extração:** Os dados são extraídos de três endpoints da PokeAPI (`/pokemon`, `/ability`, `/type`).
- **Transformação:** Os dados são transformados em dataframes pandas.
- **Carga:** Os dados transformados são carregados em um banco de dados SQLite.
- **Alertas:** Um sistema de alerta notifica falhas no processo de extração utilizando a biblioteca `plyer`.

## Instalação

Para executar este projeto, siga as instruções abaixo:

1. Clone o repositório:

   ```sh
   git clone <URL_DO_SEU_REPOSITORIO>
   cd <NOME_DO_REPOSITORIO>
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
5. **Definição da função para extrair todas as páginas de uma API**
6. **Definição da função para extrair dados das tabelas**
7. **Definição da função para carregar dados no banco de dados**
8. **Execução da extração, transformação e carga dos dados**
9. **Visualização dos dados extraídos**
10. **Exemplo de erro ao extrair uma base**

## Exemplo de Saída

Abaixo estão as primeiras linhas dos dataframes carregados no banco de dados:

### Dados dos Pokémons

| name       | url                                  |
| ---------- | ------------------------------------ |
| bulbasaur  | https://pokeapi.co/api/v2/pokemon/1/ |
| ivysaur    | https://pokeapi.co/api/v2/pokemon/2/ |
| venusaur   | https://pokeapi.co/api/v2/pokemon/3/ |
| charmander | https://pokeapi.co/api/v2/pokemon/4/ |
| charmeleon | https://pokeapi.co/api/v2/pokemon/5/ |

### Dados das Habilidades

| name         | url                                  |
| ------------ | ------------------------------------ |
| stench       | https://pokeapi.co/api/v2/ability/1/ |
| drizzle      | https://pokeapi.co/api/v2/ability/2/ |
| speed-boost  | https://pokeapi.co/api/v2/ability/3/ |
| battle-armor | https://pokeapi.co/api/v2/ability/4/ |
| sturdy       | https://pokeapi.co/api/v2/ability/5/ |

### Dados dos Tipos

| name     | url                               |
| -------- | --------------------------------- |
| normal   | https://pokeapi.co/api/v2/type/1/ |
| fighting | https://pokeapi.co/api/v2/type/2/ |
| flying   | https://pokeapi.co/api/v2/type/3/ |
| poison   | https://pokeapi.co/api/v2/type/4/ |
| ground   | https://pokeapi.co/api/v2/type/5/ |

## Contribuição

Se você quiser contribuir com este projeto, sinta-se à vontade para fazer um fork do repositório, criar uma branch para suas alterações e abrir um pull request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
