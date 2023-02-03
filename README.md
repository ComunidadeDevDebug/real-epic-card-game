# Real Epic Card Battle
>
> by Dev&Debug Initiative

## Resumo

Trata-se de um jogo virtual de cartas, baseado em turnos de ataque, defesa e magia, onde o objetivo é zerar os pontos de vida de seu oponente.  

## Conhecendo as cartas

### Atributos Comuns

As seguintes características são comuns para todas as cartas do jogo:  

#### Tipo

Existem três tipos de cartas: Cartas de Ataque, Cartas de Defesa e Cartas de Magia.  
Cada tipo tem uma função específica e só podem ser usados em momentos específicos (vide capítulo Turnos).  

#### Custo

Valor que será descontado imediatamente dos Pontos de Vida do jogador quando a carta for lançada.  

#### Nome

É a identificação única da carta.  
Ex: `“Lança sagrada”`, `“Escudo de prata”`, `“Poção do amor”`, etc …  

#### Descrição

Um pequeno texto falando sobre a carta e seus possíveis efeitos.  
Ex:
> “O ataque dessa lança não pode ser defendido por cartas de custo menor que 5”  

> “Essa poção recupera 10 pontos de vida do jogador e 5 pontos de vida do seu oponente”  

#### Imagem

<figure>
      <img src=".\docs\Images\card-example01.png" width="100px"/>
      <figcaption>
            Imagem ilustrativa para ajudar na personalização/identificação das cartas
      </figcaption>
</figure>

#### Cartas de Ataque

As Cartas de Ataque possuem um atributo chamado **Pontos de Ataque** que é a quantidade de pontos que se espera diminuir dos *Pontos de Vida* do oponente, caso não seja realizado nenhum *Movimento de Defesa* e não exista nenhuma *Magia Ativa* que influencie nesse sentido.  
Ex:  
>Foi lançada a carta “Lança sagrada” que possui 10 pontos de ataque. O oponente não fez seu Movimento de Defesa e, portanto, seus Pontos de Vida diminuem 10 pontos.  

#### Cartas de Defesa  

As Cartas de Defesa possuem um atributo chamado **Pontos de Defesa** que é a quantidade máxima de pontos que se espera diminuir de um *Movimento de Ataque* realizado pelo oponente caso não exista nenhuma *Magia Ativa* que influencie nesse sentido.  
Ex:
>O oponente lança a carta “Lança sagrada” que possui 10 pontos de ataque no seu Movimento de Ataque. Você lança a carta de defesa “Escudo de prata” que possui 9 Pontos de Defesa durante o seu Movimento de Defesa e, portanto, seus Pontos de Vida diminuem 1 ponto.  

#### Cartas de Magia  

As Caras de Magia não possuem nenhum atributo extra, porém é a sua descrição que aponta qual é o  efeito da carta lançada e quando esse efeito acontecerá.  
Ex:
>A carta “Poção do Amor” impede seu oponente de realizar o Movimento de Ataque no próximo turno.

**Importante**: o custo da carta sempre é “cobrado” no momento em que ela é lançada e só depois o efeito é verificado. Então, por exemplo, em cartas de recuperação de energia deve-se tomar cuidado para não zerar os próprios pontos antes de receber o benefício de recuperação.  
Ex:
>A carta “Cura Milagrosa” custa 3 pontos e recupera 10 Pontos de Vida. Se o jogador tiver apenas 3 PV e usar essa carta, primeiro seus PV ficam zerados (e com isso ele perde o jogo) antes de ganhar os 10 PV da carta.

#### Quantidade de Cartas

##### Quantidade de Cartas no Deck

Os jogadores devem montar um Deck (conjunto de cartas) com 60 cartas.  
Não existe um mínimo ou máximo para os tipos de cartas e cabe ao jogador balancear a quantidade de cada tipo de acordo com a sua estratégia de jogo.

##### Quantidade de Cartas na Mão

Antes do início do primeiro turno cada jogador inicia com 5 cartas na mão. Esse é também o número máximo de cartas que um jogador pode ter em mãos no final de cada Movimento dentro do turno.  
Ao final de cada turno, cada jogador recebe uma única de carta de seu monte, a menos que o efeito de uma magia altere esta quantidade.  
Ex:
> O jogador possui 5 cartas e compra mais uma no início do turno. É a sua vez de fazer um Movimento de Ataque porém ele não possui Carta de Ataque, ao encerrar o Movimento de Ataque ele deve descartar uma carta de sua mão.

Ex2:
> O jogador possui 5 cartas na mão e lança uma magia (ficando com 4 cartas na mão) que o permite comprar 3 cartas (ficando, agora, com 7 cartas na mão). Ao final do Movimento de Magia ele deve descartar 2 cartas.  

##### Quantidade de Cartas de Magia Ativas

Algumas Cartas de Magia podem ter um efeito que dura mais de um turno como, por exemplo:
> “Essa poção venenosa tira 1 PV do seu oponente no início de cada ação de ataque."  

#### Turnos

Um turno é composto por 3 movimentos diferentes e sequenciais:  

1. Um jogador inicia o turno fazendo um Movimento de ataque.

2. O oponente pode, então, fazer o Movimento de defesa.

3. Após encerrado o movimento de defesa e calculado os danos o jogador atacante pode Lançar Magia.

A cada turno os jogadores invertem os papéis, ou seja, em um turno atuam como Jogador Atacante e no turno seguinte Jogador Defensor.  

### Elementos

- **Estoque** - Total de cartas que um jogador possui. O jogador poderá ter um número ilimitado de cartas, repetidas ou não. O jogador precisará escolher 60 cartas do seu Estoque para formar um Deck.  
- **Deck** - Conjunto das 60 cartas escolhidas para iniciar uma partida.  
- **Mão** - Conjunto de cartas que o jogador tem à disposição para utilizar no turno. Máximo de 5 cartas.
- **Descarte** - Conjunto de cartas utilizadas ou descartadas durante a partida, não podem ser reutilizadas (a menos que o efeito de uma magia diga o contrário). Cada jogador possui a sua pilha de descarte contendo apenas as cartas de seu próprio Deck.  
- **Mesa** - Lugar onde são reveladas as cartas jogadas.

### Requisitos Funcionais

Micro Serviços  
Compra de cartas temáticas, skins para cartas comuns  
Compra de Avatar e melhoria de avatar  
Linguagem Rust  
Jogo em rede  
Treino contra I.A.  
Login com redes sociais  
TutorialMobile first (design vertical)  
Publicidade na versão grátis  
Jogar entre plataformas (mobile joga contra playstation)  
Compras no jogo não devem alterar a jogabilidade (fair play entre jogadores pagos e não pagos)  
Animações das cartas  
Partidas ranqueadas  
Contagem de tempo para turnos  
Chat entre participantes  
Badges  
Monorepositório  
Projeto “Dockerizado”  
Hooks entre turnos  
Termos de aceite  

### Próximos passos

- [ ] Landing page com regras do jogo;  
- [ ] Montar ambiente dev backend;  
- [x] Estruturar repositório e criara documentação usando Markdow;  
- [ ] Documentar MVP -> todo mundo

### Menor Produto Viável

[Releases](./docs/Releases.md)

-
