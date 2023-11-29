# LevelUp

![Capa do Projeto](https://as1.ftcdn.net/v2/jpg/02/60/32/86/1000_F_260328666_ZvdyDkFCAihdLyly8Xb5KGOY3eWIv61K.jpg)


<h4 align="center"> 
	🚧  Em desenvolvimento . . .
</h4>

# Índice/Sumário
* [Sumário](#índice/sumário)
* [Introdução](#introdução)
* [1.1.Objetivos](# 1.1.Objetivos)
* [Tecnologias Usadas](#tecnologias-usadas)
* [Metodologias](#metodologias)
* [Dicionário de Dados](#Dicionário-de-Dados)
* [Configuração do Ambiente](#Configuração-do-Ambiente)
* [Leitura de Dados](#Leitura-de-Dados)
* [Organização E Limpeza de Dados](#Organização-E-Limpeza-de-Dados)
* [Mapeamento de Dados](#Mapeamento-de-Dados)
* [Feature Engineering](#Feature-Engineering)
* [Análise dos Dados](#Análise-dos-Dados)
* [Observações](#Observações)
* [Contribuição](#contribuição)
* [Licença](#licença)
* [Referências](#Referências)
* [Agradecimentos](#agradecimentos)
* [Autores](#autores)



# 1.0 Introdução
A LevelUp é uma empresa especializada no desenvolvimento de jogos eletrônicos para a plataforma Steam e desejamos criar jogos inovadores que despertem o interesse do público. Para isso decidimos realizar uma análise exploratória de dados profunda sobre os dados da Steam relacionados aos jogos disponíveis na mesma, para que assim, possamos descobrir quais os melhores gêneros e tipos para que possamos investir nosso tempo e trabalho. 

A Steam é uma plataforma de distribuição de jogos digitais para computadores (Windows, macOS e Linux). Por meio dela é possível que consumidores comprem ou ativem jogos dentro do serviço. Possui um programa cliente, que deve ser instalado no computador, para que os jogos possam ser executados, mantendo tudo atualizado. 

Para tal estudo de dados, iremos utilizar alguns datasets sobre a Steam disponíveis em [Kaggle](https://www.kaggle.com/), sendo estes arquivos CSV, os quais serão:
 [Steam-Releases](https://www.kaggle.com/datasets/whigmalwhim/steam-releases), [Steam-Games](https://www.kaggle.com/datasets/thedevastator/get-your-game-on-metacritic-recommendations-and), [Steam-Games-Dataset](https://www.kaggle.com/datasets/nikatomashvili/steam-games-dataset), contendo vasta informação sobre a grande biblioteca de jogos presente na Steam.

Algumas destas informações são:
* Nome dos Jogos;
* Gênero;
* Data de Lançamento;
* Maior quantidade de Jogadores;
* Jogos Vendidos;
* Recomendações;
* Avaliações de Jogadores;
* Avaliações de Crítica;

# 1.1.Objetivos

O objetivo deste estudo é realizar uma Análise Exploratória dos Dados (Exploratory Data Analysis - EDA) do conjunto de dados sobre a Steam, adaptada pelos autores e disponível em *****************, a fim de caracterizar os perfis dos jogos disponíveis na plataforma Steam. 

Especificamente serão respondidas as seguintes questões de pesquisa:

    1- Tendo em vista os Bancos de Dados escolhidos, o gênero do jogo tem
    impacto direto no sucesso do jogo, na questão relacionado a jogadores que jogam?

    2- Tendo em vista os Bancos de Dados escolhidos, a época do ano de lançamento do jogo têm impacto direto em seu sucesso?

    3- Tendo em vista os Bancos de Dados escolhidos, qual a porcentagem das avaliações sejam elas positivas
    ou negativas para a quantidade de jogadores que compraram os jogos? É um número aceitável? 

    4- Tendo em vista os Bancos de Dados escolhidos, as notas de sites especializados em análise de jogos
    são equivalentes às recomendações dos jogadores?


# 1.2 Tecnologias Usadas

- [MongoDB](https://www.mongodb.com/pt-br)
- [Kaggle](https://www.kaggle.com/)

# 2.0 Metodologias
Nesta seção será apresentado todo o processo de preparação, organização e limpeza de dados feito no dataset que possui os seguintes dados:


# 2.1 Dicionário de Dados

 Colunas | Descrição  |  Tipo   |  Formato do Campo
--------- | ------ | ------ | ------
ResponseName     | Nome do Jogo   |  Texto  |  String
Titlle          | Nome do Jogo    |  Texto   | String
ReleaseDate    | Data de Publicação do Jogo    | Data   |  yyyy-mm-dd
OrigianlPrice  | Preço Original   |  Número   | Float
PeakPlayers |  Pico de Jogadores    | Número   | Int
AllTimePeakDate | Data do Pico de Jogadores | Número   | Int
Metacritic    | Nota Metacrítica  | Número  | Float
Recommendations  | Recomendação  | Número  | Int
AllReviewsSummary | Sumário de Todas as Reviews  | Porcentagem  |  00%
PrimaryGenre | Gênero Primário  |  Texto  | String
StoreGenres  | Gênero da Loja   |  Texto  | String

# 2.2 Observações
* `ResponseName` e `Tittle` se referem ao `Nome do Jogo`;
* `Recommendations` é levado em consideração a recomendação dos jogadores;
* Em `PrimaryGenre` é levado em consideração apenas o gênero principal do jogo, não sendo levado em consoderação tags de loja.
* `StoreGenres` se refere às tags da loja da Steam (Exemplo: Multiplayer, Singleplayer);

# 2.3 Configuração do Ambiente

# 2.4 Leitura de Dados

# 2.5 Organização E Limpeza de Dados

# 2.6 Mapeamento de Dados

# 2.7 Feature Engineering

# 3.0 Análise dos Dados


# Contribuição

Leia o arquivo [CONTRIBUTING.md](CONTRIBUTING.md) para saber detalhes sobre o nosso código de conduta e o processo de envio de solicitações *pull* (*Pull Request*) para nós.


# Licença

Este projeto está licenciado sob a Licença MIT,  consulte o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.


# Referências
[Tecnoblog - Steam](https://tecnoblog.net/responde/o-que-e-steam-tudo-sobre-a-loja-valve/)

# Agradecimentos

Seção livre para você agradecer a todos que contribuiram para a execução do seu projeto.


# Autores

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/111711621?v=4" width="100px;" alt="Leonardo Nunes"/><br /><sub><b>Leonardo Nunes</b></sub></a><br /><a href="https://github.com/sLeoNunes" title="Readme, Documentation, Ideas, Search">📝📖💻🤔</a>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/85580881?v=4" width="100px;" alt="Carla Coutinho"/><br /><sub><b>Carla Coutinho</b></sub></a><br /><a href="https://github.com/MonHardy" title="Documentation, Ideas, Search">📖💻🤔</a></td>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/130943420?v=4" alt="Samuel Maciel"/><br /><sub><b>Samuel Maciel</b></sub></a><br /><a href="https://github.com/Sn0wSA" title="Search, Ideas, Bug Report">💻🤔🐛</a></td>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/80545302?v=4" width="100px;" alt="Lucas Alexandre"/><br /><sub><b>Lucas Alexandre</b></sub></a><br /><a href="https://github.com/Lucas-AlexNK" title="Search, Ideas">💻🤔</a></td>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/113992861?v=4" width="100px;" alt="Diego Diniz"/><br /><sub><b>Diego Diniz</b></sub></a><br /><a href="https://github.com/DiegoDiniz59" title="Readme, Search, Ideas">📝💻🤔</a></td>
      <td align="center" valign="top" width="14.28%"><img src="https://avatars.githubusercontent.com/u/89555246?s=400&u=51041b9b462ada2485b67ba84d947db1239b2835&v=4" width="100px;" alt="Gabriel Gontijo"/><br /><sub><b>Gabriel Gontijo</b></sub></a><br /><a href="https://github.com/Gontijo23" title="Bug Report, Search, Ideas">🐛💻🤔</a>
    </tr>

