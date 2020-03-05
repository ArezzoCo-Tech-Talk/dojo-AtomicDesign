# Atomic Design

O conceito de criar padrões arquitetônicos surge no livro ["Uma linguagem de padrões"](https://statics-submarino.b2w.io/sherlock/books/firstChapter/112900425.pdf):

> Os elementos dessa linguagem são entidades chamadas de padrão. Cada padrão descreve um problema que ocorre repetidas vezes em nosso meio ambiente e então descreve o ponto central da solução do problema, de modo que você possa usar a mesma solução milhares de vezes, mas sem jamais ter de repeti-la.

- cada componente é um padrão
- cada componente se repete várias vezes nos sites
- uma vez que o componente está criado só precisamos usar ele e não criá-lo novamente

----

No exemplo do livro sobre as praças fala que uma praça é constituída por vários elementos, como muro ambiente para caminhar, enquanto também a praça faz parte de algo maior que são bairros

> Esta ordem, apresentada em uma sequência linear, é essencial ao modo como a ordem funciona. Isso será apresentado e explicado com mais detalhes na próxima seção. O mais
importante quanto a esta sequência é que ela se baseia nas
conexões entre os padrões. Cada padrão está conectado a certos padrões “maiores”(ou mais abrangentes), que estão acima
dele, e a certos padrões “menores”(ou mais específicos) que
estão abaixo, na linguagem. O padrão ajuda a completar aqueles padrões maiores e, ao mesmo tempo, é completado pelos
padrões menores

> Em suma, nenhum padrão é uma entidade isolada. Cada
padrão existe somente porque é sustentado por outros padrões:
os padrões maiores, dentro dos quais ele se inclui, os padrões do
mesmo tamanho, que o circundam, e os padrões menores, nele
inserido

Uma Linguagem de Padrões
