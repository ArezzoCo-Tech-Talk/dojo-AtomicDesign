# Atomic Design

O conceito de criar padrões arquitetônicos surge no livro ["Uma linguagem de padrões"](https://statics-submarino.b2w.io/sherlock/books/firstChapter/112900425.pdf):

> Os elementos dessa linguagem são entidades chamadas de padrão. Cada padrão descreve um problema que ocorre repetidas vezes em nosso meio ambiente e então descreve o ponto central da solução do problema, de modo que você possa usar a mesma solução milhares de vezes, mas sem jamais ter de repeti-la. (Uma linguagem de padrões)

- cada componente é um padrão
- cada componente se repete várias vezes nos sites
- uma vez que o componente está criado só precisamos usar ele e não criá-lo novamente

> Cada padrão está conectado a certos padrões "maiores"(ou mais abrangentes), que estão acima dele, e a certos padrões "menores"(ou mais específicos) que estão abaixo, na linguagem. O padrão ajuda a completar aqueles padrões maiores e, ao mesmo tempo, é completado pelos padrões menores. (Uma linguagem de padrões)

- os componentes são formados por outros componentes.

No exemplo do livro sobre as praças fala que uma praça é constituída por vários elementos, como muro e ambiente para caminhar, enquanto também a praça faz parte de algo maior que são bairros e as cidades.

## Atomic design

[Atomic desgin](https://bradfrost.com/blog/post/atomic-web-design/) implementa essa forma de enxergar os padrões.

Os componentes ficam pequenos, pois a implementação de partes deles está em outro lugar.

O componente deve ser auto-suficiente e isso é percebido quando colocado no guia de estilos.

### Tipos

A classificação dos componente, ao meu ver, é algo discutível e situacional, apenas usado para organizar o conteúdo sem ficar tudo no mesmo lugar.

O tipo do componente é definido pelo seu CSS e não pelo HTML, um componente como um `container` que engloba a página toda mas em seu CSS ele apenas cuida de seu estilo deve ser um componente menor.

São classificados como:

- **átomos** vão ter o estilo deles apenas.
- **moléculas** serão componentes que necessariamente são compostos por átomos e talvez outras moléculas específicas.
- **organismos** os componentes organismos começam a ter as características mais próximas da aplicação, então por vezes eles ficam mais extensos, pois sobrescrevem mais os os componentes que o compõe.
- **templates** então são as partes prontas que irão compor uma página. `header`, `footer`, `main`...
- **pages** não sei

### Implementando

![image](https://user-images.githubusercontent.com/27368585/75980958-42774300-5ec2-11ea-9d9f-53ce34ea2992.png)

Nessa imagem de um cabeçalho o ícone se repete 3x, logo ele é um componente e pode ser reaproveitado.

```css
.icon {
  width: 100%;
  max-width: 30px
}
```


## Dúvidas frequentes

**"Tudo é um componente..." Mas e a página?** Bom, o a página vai fazer o mesmo que os componentes fazem que é estilizar os componentes menores.

**Quais componentes eu faço primeiro?** Os menores, porque nenhum componente deve saber quem vai renderizá-lo, enquanto sabe o que vai renderizar e, pensando em ser auto-suficiente, ele precisa fazer isso bem.

**Quando eu devo desconfiar que estou fazendo errado?** Principalmente quando o CSS se estende muito. Em regra, mais de 50 linhas já da para desconfiar fortemente.

**Por que é importante todos entenderem?** Para todos juntos concordarem e fazerem junto.

