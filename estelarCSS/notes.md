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

### Regra important

Sobrescreve tudo, contudo não é uma boa prática

### at-rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido do indentificador e valor

## Exemplos comuns 

- @important /* incluir um CSS externo */ 
- @media /* regras condicionais para dispositivos */
- @font-face /* fontes externas */
- @keyframes /* Animation */

### Funções

* Nome seguido de abre e fecha parenteses
* Recebe argumentos

{
  color:rgb(255, 0 ,100);
  width: calc(100% - 10px);
}

### Vendor Prefixes

Permite que browsers adicione `features`
a fim de colocar em uso alguma novidade que vemos no CSS

# Exemplo

p {
	-webkit-background-clip: text; /*Chrome, Safari, iOS e Android*/
	-moz-background-clip: text; /* Mozilla (Firefox) */
	-ms-background-clip: text; /* Internet Explorer ou Edge*/
	-o-background-clip: text; /* Opera */
}

**`Consultas`**

https://ireade.github.io/which-vendor-prefix

https://caniuse.com

