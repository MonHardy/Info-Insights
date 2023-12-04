# LevelUp

![Capa do Projeto](https://as1.ftcdn.net/v2/jpg/02/60/32/86/1000_F_260328666_ZvdyDkFCAihdLyly8Xb5KGOY3eWIv61K.jpg)


<h4 align="center"> 
	✅  Trabalho Finalizado!
</h4>

# Índice/Sumário
* [Sumário](#índice/sumário)
* [Introdução](#introdução)
* [Objetivos](#objetivos)
* [Tecnologias Usadas e Ferramentas](#tecnologias-usadas-e-ferramentas)
* [Metodologias](#metodologias)
* [Dicionário de Dados](#Dicionário-de-Dados)
* [Observações](#Observações)
* [Configuração do Ambiente](#Configuração-do-Ambiente)
* [Leitura de Dados](#Leitura-de-Dados)
* [Organização E Limpeza de Dados](#Organização-E-Limpeza-de-Dados)
* [Mapeamento de Dados](#Mapeamento-de-Dados)
* [Análise dos Dados](#Análise-dos-Dados)
* [Conclusão](#conclusão)
* [Contribuição](#contribuição)
* [Referências](#Referências)
* [Agradecimentos](#agradecimentos)
* [Autores](#autores)


# Introdução
A LevelUp é uma empresa especializada no desenvolvimento de jogos eletrônicos para a plataforma Steam e desejamos criar jogos inovadores que despertem o interesse do público. Para isso decidimos realizar uma análise exploratória de dados profunda sobre os dados da Steam relacionados aos jogos disponíveis na mesma, para que assim, possamos descobrir quais os melhores gêneros e tipos para que possamos investir nosso tempo e trabalho. 

A Steam é uma plataforma de distribuição de jogos digitais para computadores (Windows, macOS e Linux). Por meio dela é possível que consumidores comprem ou ativem jogos dentro do serviço. Possui um programa cliente, que deve ser instalado no computador, para que os jogos possam ser executados, mantendo tudo atualizado. 

Para tal estudo de dados, iremos utilizar alguns datasets sobre a Steam disponíveis em [Kaggle](https://www.kaggle.com/), sendo estes arquivos CSV, os quais serão:
 [Steam-Releases](https://www.kaggle.com/datasets/whigmalwhim/steam-releases) e [Steam-Games](https://www.kaggle.com/datasets/thedevastator/get-your-game-on-metacritic-recommendations-and), contendo vasta informação sobre a grande biblioteca de jogos presente na Steam.

Algumas destas informações são:
* Nome dos Jogos;
* Gênero;
* Data de Lançamento;
* Maior quantidade de Jogadores;
* Jogos Vendidos;
* Recomendações;
* Avaliações de Jogadores;
* Avaliações de Crítica;

# Objetivos

O objetivo deste estudo é realizar uma Análise Exploratória dos Dados (Exploratory Data Analysis - EDA) do conjunto de dados sobre a Steam, adaptada pelos autores e disponível em [game_data_all.csv](https://github.com/MonHardy/level-up/blob/main/game_data_all.csv) e [games-features-edit.csv](https://github.com/MonHardy/level-up/blob/main/games-features-edit.csv), a fim de caracterizar os perfis dos jogos disponíveis na plataforma Steam. 

Especificamente serão respondidas as seguintes questões de pesquisa:

    1- O gênero do jogo tem impacto direto no sucesso do jogo?

    2- A época do ano de lançamento do jogo têm impacto direto em seu sucesso?

    3- Há alguma relação entre o número das avaliações, sejam elas positivas ou negativas, para a quantidade de jogadores que compraram os jogos?

    4- As notas de sites especializados em análise de jogos são equivalentes às recomendações dos jogadores?


# Tecnologias Usadas e Ferramentas

- [Google Colab](https://colab.research.google.com/)
- [Kaggle](https://www.kaggle.com/)
- [Linguagem de Programação Python](https://www.python.org/)

# *Metodologias*
Nesta seção será apresentado todo o processo de preparação, organização e limpeza de dados feito no dataset que possui os seguintes dados:


# Dicionário de Dados

 Colunas | Descrição  |  Tipo   |  Formato do Campo
--------- | ------ | ------ | ------
response_name     | Nome do Jogo   |  Texto  |  [A-z]
game     | Nome do Jogo   |  Texto  |  [A-z]
release    | Data de Publicação do Jogo    | Data   |  yyyy-mm-dd
price_initial  | Preço Original   |  Número   | [0.0]
peak_players |  Pico de Jogadores    | Número   | [0-9]
metacritic    | Nota Metacrítica  | Número  | [0.0]
recommendations  | Recomendação  | Número  | [0-9]
recommendation_count  | Total de Recomendação  | Número  | [0-9]
total_reviews |  Todas as Reviews  | Número  |  [0-9]
rating | Notas/Avaliação  | Número  |  [0.0]
primary_genre | Gênero Primário  |  Texto  | [A-z]
store_genres  | Gênero da Loja   |  Texto  | [A-z]

# Observações
* `response_name`, `game` se referem ao `Nome do Jogo`;
* `recommendations` é levado em consideração a recomendação dos jogadores;
* Em `primary_genre` é levado em consideração apenas o gênero principal do jogo, não sendo levado em consoderação tags de loja.
* `store_genres` se refere às tags da loja da Steam (Exemplo: Multiplayer, Singleplayer);

# Configuração do Ambiente

Para darmos início a Análise de Dados, escolhemos o Google Colab como nossa ferramenta de trabalho e para isto, realizamos imports, tais como NumPy e Pandas.

<img src="https://github.com/MonHardy/level-up/blob/main/Capturar.PNG?raw=true"/>

# Leitura de Dados

No Google Colab, realizamos o upload dos bancos de dados no Colab.

[Trabalho Análise de Dados](https://colab.research.google.com/drive/1fBp_at-FOFNTRc25hlo6kwKGCBPUPjPG#scrollTo=dITIWsW2WaQU)

# Organização E Limpeza de Dados

Após escolhermos os datasets a serem utilizados, percebemos que haviam certas colunas de dados que não iriamos utilizar, então decidimos por retirá-las, a fim de diminuir o tamanho dos datasets.

Diante disso, optamos por retirar as seguintes colunas do Dataset "Steam Releases":

![image](https://github.com/MonHardy/level-up/assets/111711621/1de038c1-4b31-4961-9cde-83ae4a267253)

Já no Dataset "Steam Games" decidimos por retirar algumas colunas:

![image](https://github.com/MonHardy/level-up/assets/111711621/6ed7bf95-14ec-4c37-b121-8262ed773d6f)


# Mapeamento de Dados

Para melhorar a análise e interpretação dos dados os seguintes atributos serão modificados:

[game_data_all.csv](https://github.com/MonHardy/level-up/blob/main/game_data_all.csv)

 Colunas | Original  |  Modificado 
--------- | ------ | ------ 
primary_genre    | Unknown Genre  |  -
primary_genre    | Free To Play  |  -
primary_genre    | Early Acess  |  -
primary_genre    | Nudity  |  -
primary_genre    | Sexual Content |  -

![image](https://github.com/MonHardy/level-up/assets/111711621/f6cc604f-bdb4-4228-869d-5561704443cb)

Decidimos por retitar os gênero que não serão utilizados em nossa análise.


[games-features-edit.csv](https://github.com/MonHardy/level-up/blob/main/games-features-edit.csv):

 Colunas | Original  |  Modificado 
--------- | ------ | ------ 
Metacritic    | 0  |  50

![image](https://github.com/MonHardy/level-up/assets/111711621/cb086e94-20b8-4062-bf1c-48186ef87f93)

Decidimos por alterar os valores '0' em Metacritic por '50', pois 50 é considerado uma nota neutra, nem positiva e nem negativa, o que nos possibilita trabalhar com algum valor neste parâmetro.


# Análise dos Dados


    1- O gênero do jogo tem impacto direto no sucesso do jogo?
    
![image](https://github.com/MonHardy/level-up/assets/111711621/05cd8874-fb21-4c16-bceb-689f11cf004b)

Sim. De acordo com os dados avaliados, os jogos do gênero Action são comumente mais jogados do que os outros gêneros. 


    2- A época do ano de lançamento do jogo têm impacto direto em seu sucesso?

![image](https://github.com/MonHardy/level-up/assets/111711621/363a3ab0-b7b8-4b1c-8671-224cb72dbae0)

Sim. A época de férias tem resultado em vendas maiores do que as outras épocas. Fevereiro, por exemplo, quando ocorrem as férias na Ásia, costumam ter lançamentos de maiores sucessos.

    3- Há alguma relação entre o número das avaliações, sejam elas positivas ou negativas, 
    para a quantidade de jogadores que compraram os jogos?
    
![image](https://github.com/MonHardy/level-up/assets/111711621/a9466fba-56aa-456c-85f9-932a001f0e1f)

Não necessariamente, há casos em que jogos com muitos jogadores possuem a mesma média de avaliação de que jogos com poucos jogadores.

    4- As notas de sites especializados em análise de jogos são equivalentes às recomendações dos jogadores?
    
![image](https://github.com/MonHardy/level-up/assets/111711621/a3ac0bf1-240a-49b0-a3be-8e624cb45145)

Não necessariamente, há casos em que as notas da crítica especializada diverge das recomendações dos jogadores que jogaram o jogo.


# Conclusão

Após a realização da análise de dados, nós da LevelUp percebemos que, para termos mais sucesso em nosso futuro jogo, é de extrema importância que o mesmo seja do gênero Ação ou Aventura, visto que estes dois gêneros se destacaram no quesito de pico de jogadores, cabendo a nós decidirmos internamente qual será o escolhido. Além deste fator, é imprescindível que lançemos nosso jogo em um período de férias nos países mais populosos, pois haverá mais chances de ser jogado, possibilitando um grande retorno financeiro.

Ademais, vale ressaltar que devemos focar a criação de nosso jogo nas questões que agradem ao público e não somente às questões que agradam mídias especializadas em avaliações, pois as avaliações dos jogadores tem o potencial de convencer outros possíveis jogadores a testar nosso jogo, fazendo com que engajem nosso projeto.



# Contribuição

*Participação e contribuição dos Alunos:*

- Carla Monique
- Diego Diniz
- Gabriel Gontijo
- Leonardo Nunes
- Lucas Alexandre
- Samuel Maciel

*E auxílio do Professor Diego Augusto Barros*



# Referências
- [Tecnoblog - Steam](https://tecnoblog.net/responde/o-que-e-steam-tudo-sobre-a-loja-valve/)
- [Steam-Releases](https://www.kaggle.com/datasets/whigmalwhim/steam-releases)
- [Steam-Games](https://www.kaggle.com/datasets/thedevastator/get-your-game-on-metacritic-recommendations-and) 
- [Steam-Games-Dataset](https://www.kaggle.com/datasets/nikatomashvili/steam-games-dataset)

# Agradecimentos

Agradecemos ao professor Diego por nos ter dado a oportunidade de desenvolver este projeto, possibilitando que colocássemos nosso aprendizado adquirido em sala de aula, através de suas aulas, em prática.


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

