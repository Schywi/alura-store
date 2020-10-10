## Grid

Funciona com base em linhas e colunas


Define quanto de espaço cada linha e coluna da div vai ter


Para calcular o tamanho do grid usa:

height: calc(100vh - 50px)

onde 50px é o tamanho do cabeçalho




Logica do css: metodologia BEM

.destaques__principal{}

destaqies = bloco
principal = elemento filho de destaques.


## Posicionando elementos


usamos : grid-column-start: 1;
grid-column-end: 3; pra definir a coluna que o elemento vai terminar.


para linha troca column por row;

Para prencher a quantidade de linhas e colunas que desejamos devemos adicionar 1 ao numero


nth-child(2): pega o segundo filho do elemento

`.destaques__secundario:nth-child(2)`

Para informar que a posição e o tamanho vão ser na msm linha do css usa:

`background: url()... center/cover no-repeat`

Atalhos pro grid: grid-column: 1 / 2;
primeiro parametro é onde ele começa e segundo parametro é onde ele termina. o msm vale pro row.

Para visualizar o grid use o console.log.


## Estilizando os destaques

Para erdar algo do elemento pai usa `inherit`

a classe  destaque ditulo adiciona uma bordinha nos itens
```

.destaques__titulo {
    background: rgba(0, 0, 0, .5);
    color: #fdfdfd;
    padding: .6rem;
    text-align: center;
    width: 100%;
}

```
Para definir um espaçamento entre as colunas usa `grid-gap`

Para dizer onde algo deve comelar no grid layout usa :

```
  grid-column-start
grid-column-end
grid-row-start
grid-row-end
```
Ou  `grid-row: 1 / 3;`

Para preencher tudo vc adiciona 1 a mais

**...................//...............**

`grid-template-areas` : vc define as ateas que seu template vai ter ex:

```
grid-template-areas:
        "card-imagem"
        "card-corpo";
```
usa tambem `grid-template-columns: 100%;`

Podemos definir onde o elemento vai ficar dentro do grid ao informar qual o nome do `grid-area`ele vai ocupar :

```
populares__card___imagem {
    grid-area: card-imagem;
    height: 100%;
    width: 100%;
}
```

Usamos toda hora esse grid-area para definir os elementos que ficam dentro do grid


Quando o tamanho dos cards ficarem mto grande ele quebra pra proxima linha;

## Aula 4 Estilizando o cabeçalho

Os arquivos CSS ja dizem tuto


# Aula 5

Na responsividade do site usamos o seguinte padrão :

```
@media screen and (min-width:0) {}

@media screen and (min-width: 768px) {}

@media screen and (min-width: 992px) {}

@media screen and (min-width:1200px) {}

```

Essse codigo esconde os grid;
```

    .destaques__secundario:nth-child(2) {
        display: none;
        grid-column: none;
        grid-row: none;
    }
```
Trem do flexbox :
Lembra da propriedade align-items que colocávamos no flex container? O align-self faz a mesma coisa, só que alinha um único elemento e é colocada no flex item.
