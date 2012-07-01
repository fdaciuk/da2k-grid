# Overview

Já existem muitos sistemas de grid por aí, mas eles têm 2 problemas:

1. Já tem uma largura, margem de espaçamento e número de colunas padrão;
2. Deixam o seu HTML "sujo" por ter que incluir muitas classes.

* * *

A ideia do **Da2kGrid** é ser um grid dinâmico, usando [SASS](http://sass-lang.com/) para que você mesmo possa definir a largura, margem de espaçamento e número de colunas do seu grid, mas definindo esses valores somente no CSS, mantendo o seu HTML limpo e organizado :)

## Como usar

1. Edite o arquivo **da2k-grid.scss** e, nas primeiras linhas, defina a largura total do grid **($width)**, a quantidade de colunas **($columns)** e o espaçamento entre as colunas **($col_margin)**;

> PS.: A margem entre as colunas **($col_margin)** será dividida por 2, e colocado metade em cada lado da coluna como **margin**, por isso, use somente números PARES!

2. Inclua o arquivo **da2k-grid.scss** no seu arquivo SASS principal **(style.scss)**, por exemplo.

3. Para o container principal, que ocupará toda a área útil (com a largura definida no arquivo do grid), inclua o mixin *row*:

`#main { @include row }`

4. Então, para cada elemento que você quiser setar um número de colunas, use o mixin *col*, setando o número de colunas:

`#main section { @include col(12) }`