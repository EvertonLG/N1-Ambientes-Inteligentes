# N1-Ambientes-Inteligentes
# Análise Exploratória do Conjunto de Dados MovieLens (Small)

Este repositório contém uma análise exploratória inicial do conjunto de dados MovieLens (Small). O objetivo é entender a estrutura dos dados, identificar possíveis problemas e preparar os arquivos para futuras análises.

## Descrição Geral do Dataset

O conjunto de dados MovieLens (Small) contém 100.000 avaliações e 3.600 marcações aplicadas a 9.000 filmes por 600 usuários. Os dados foram coletados entre 29 de março de 1996 e 24 de setembro de 2018. Ele é amplamente utilizado para pesquisas em sistemas de recomendação e análise de preferências cinematográficas.

## Arquivos do Dataset

- **ratings.csv**: Contém as avaliações de filmes feitas pelos usuários.
- **movies.csv**: Lista de filmes disponíveis no conjunto de dados.
- **tags.csv**: Marcações (tags) atribuídas pelos usuários a determinados filmes.
- **links.csv**: Identificadores que conectam os filmes do MovieLens a bancos de dados externos (IMDb e TMDb).

## Atributos e Tipos de Dados

### ratings.csv

- `userId` (int): Identificador do usuário que fez a avaliação.
- `movieId` (int): Identificador do filme avaliado.
- `rating` (float): Nota atribuída ao filme (escala de 0,5 a 5,0).
- `timestamp` (int): Data e hora da avaliação no formato Unix epoch.

### movies.csv

- `movieId` (int): Identificador do filme.
- `title` (string): Título do filme.
- `genres` (string): Gêneros do filme, separados por `|`.

### tags.csv

- `userId` (int): Identificador do usuário que atribuiu a tag.
- `movieId` (int): Identificador do filme ao qual a tag foi atribuída.
- `tag` (string): Texto da tag.
- `timestamp` (int): Data e hora da atribuição da tag em formato Unix epoch.

### links.csv

- `movieId` (int): Identificador do filme no MovieLens.
- `imdbId` (int): Identificador do filme no IMDb.
- `tmdbId` (int): Identificador do filme no TMDb.

## Problemas Identificados e Correções Aplicadas

### Problemas Encontrados

- O campo `timestamp` está em formato Unix epoch, dificultando a leitura.
- A coluna `genres` contém múltiplos gêneros separados por `|`.
- Possíveis valores nulos e duplicatas nos arquivos.

### Correções Realizadas

- Conversão dos timestamps para um formato de data legível (`YYYY-MM-DD HH:MM:SS`).
- Separação dos gêneros em listas.
- Verificação e remoção de valores nulos e duplicatas.
- Salvamento dos arquivos limpos com o sufixo `_clean.csv`.


## Licença

Os dados são disponibilizados sob a licença do [GroupLens Research](https://grouplens.org).

