### Origiem de estilo

inline > tag style > tag link

### Especificidade

É um cálculo, onde, cada tipo de seletor e origem de estilo, possuem valores a serem
considerados

<!-- prettier-ignore -->
0. Universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e atribute selectors ([type="radio"])
100. ID selector. Inline
1000. Inline

<!--
*Vale 0*
* {
  color: red;
}

*Vale 1*
h1 {
  color: green;
}

*Vale 10*
.title {
  color: blue;
}

*Vale 100*
#my-title {
  color: gray;
}

*Vale 111*
h1.title#my-title {
  color: yellow;
}

*Vale 1000*
<h1 style="color: orange";>Olá mundo</h1>

 -->
