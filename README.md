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
│ ├── share/ </br>
│ ├── pyvenv.cfg </br>
│ </br>
├── pokeapi.db </br>
├── README.md </br>
├── requirements.txt </br>

## Funcionalidades

- **Extração:** Os dados são extraídos de três endpoints da PokeAPI (`/pokemon`, `/ability`, `/type`).
- **Transformação:** Os dados são transformados em dataframes pandas.
- **Carga:** Os dados transformados são carregados em um banco de dados SQLite.
- **Alertas:** Um sistema de alerta notifica falhas no processo de extração utilizando a biblioteca `plyer`.
- **Visualizações:** Validação de hipóteses levantadas utilizando as bibliotecas `seaborn` e `matplotlib`.

## Instalação

Para executar este projeto, siga as instruções abaixo:

1. Clone o repositório:

   ```sh
   git clone <URL_DO_SEU_REPOSITORIO>
   cd <NOME_DO_REPOSITORIO>
   ```

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

1. **Estrutura do Notebook**
2. **Instalação das bibliotecas necessárias**
3. **Importação das bibliotecas**
4. **Definição da função de alerta**
5. **Definição da função para extrair dados da API**
6. **Definição da função para extrair todas as páginas de uma API**
7. **Definição da função para extrair dados das tabelas**
8. **Definição da função para carregar dados no banco de dados**
9. **Execução da extração, transformação e carga dos dados**
10. **Visualização dos dados extraídos**
11. **Exemplo de erro ao extrair uma base**
12. **Função para executar uma consulta e retornar um DataFrame**
13. **Visualizando as tabelas**
14. **Hipóteses e Visualizações**

## Exemplo de Saída

Abaixo estão as primeiras linhas dos dataframes carregados no banco de dados:

### Dados dos Pokémons

| id  | nome       | experiencia_base | altura | peso | id_habilidade_1 | id_habilidade_2 | id_tipo_1 | id_tipo_2 |
| --- | ---------- | ---------------- | ------ | ---- | --------------- | --------------- | --------- | --------- |
| 1   | bulbasaur  | 64               | 7      | 69   | 65              | 65              | 12        | 4         |
| 2   | ivysaur    | 142              | 10     | 130  | 65              | 65              | 12        | 4         |
| 3   | venusaur   | 263              | 20     | 1000 | 65              | 65              | 12        | 4         |
| 4   | charmander | 62               | 6      | 85   | 66              | 66              | 10        | NaN       |
| 5   | charmeleon | 142              | 11     | 190  | 66              | 66              | 10        | NaN       |

### Dados das Habilidades

| id  | nome        | efeito                                            |
| --- | ----------- | ------------------------------------------------- |
| 19  | shield-dust | Ein Pokémon mit dieser Fähigkeit ist immun geg... |
| 34  | chlorophyll | Während strong sunlight ist die speed eines P...  |
| 44  | rain-dish   | Pokémon mit dieser Fähigkeit heilen am Ende je... |
| 50  | run-away    | Pokémon mit dieser Fähigkeit können immer aus...  |
| 65  | overgrow    | When this Pokémon has 1/3 or less of its HP re... |

### Dados dos Tipos

| id  | nome   |
| --- | ------ |
| 3   | normal |
| 4   | poison |
| 7   | bug    |
| 10  | fire   |
| 11  | water  |
| 12  | grass  |

## Visualização e Análises Realizadas

### Distribuição da Experiência Base dos Pokémons

A análise da distribuição da experiência base dos pokémons mostra que a maioria dos pokémons tem uma experiência base entre 50 e 200. Há alguns picos significativos que indicam que certos pokémons têm experiência base específica que é mais comum.

![Histograma da experiência base dos Pokémons](https://i.imgur.com/NoOvdLw.png)

### Correlação entre Altura, Peso e Experiência Base

A matriz de correlação entre altura, peso e experiência base mostra que há uma correlação positiva **moderada** entre altura e peso. A correlação entre experiência base e peso é mais **fraca**, mas ainda positiva, indicando que pokémons mais pesados tendem a ter uma experiência base ligeiramente maior. A correlação entre experiência base e altura é a **mais fraca** entre as três.

![Matriz de correlação entre experiência base, peso e altura dos Pokémons](https://i.imgur.com/Iax7ISf.png)

> Para mais análises e visualizações, veja o [notebook completo](https://github.com/matheusvazdata/projeto_final_etl_coderhouse/blob/main/notebooks/etl_pipeline.ipynb).

## Contribuição

Se você quiser contribuir com este projeto, sinta-se à vontade para fazer um fork do repositório, criar uma branch para suas alterações e abrir um pull request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
