## tag form

Action = para onde será enviado o formulário
method = ação a ser realizada com os dados

`<form action="" method="get">`

## tag input

Datalist = Lista de dados para selecão em um input de dados. Sempre está relacionado à um input

`<input type="text" list="fruitsdata" placeholder="Escolha uma fruta" />

<datalist id="fruitsdata">
<option>Maçã</option>
<option>Banana</option>
<option>Uva</option>
<option>Melância</option>
<option>Laranja</option>
</datalist>

<input type="color" list="colordata" placeholder="Escolha uma cor" />

<datalist id="colordata">
<option>#ff0000</option>
<option>#00ff00</option>
<option>#0000ff</option>
</datalist>`

*Atributos Comuns*

- autocomplete - completa conforme frequência de uso
- autofocus - foco
- disabled - não permite alterações
- readonly - não permite alterações, mas mantem o aspecto de ativo
- value - valor do input
- form - submeter uma tag de formulário que esteja fora do <form> (quase todos)
- required - dado obrigatório (quase todos)
- placeholder - (password, search, tel, text, url) (quase todos)
     
`<input type="text" placeholder="Digite seu nome" />`

*Atributo password*

- minlength - número mínimo de caracteres para o campo
- maxlength - número máximo de caracteres para o campo
- size - tamanho do campo visualmente
- pattern - expressão regular para validar o que está sendo digitado no campo [regra]{min,max}
- title - acompanha as mensagens de alerta no box password
- placeholder - informação no campo do que deve ser realizado
- disabled - não permite alterações
- readonly - não permite alterações, mas mantem o aspecto de ativo
- required - dado obrigatório
- inputmode - habilita o teclado em smartphone
- autocomplete 
      * on - permite a sugestão de: new-password ou current-password
      * off - desabilita a opção de autocompletar
      * new-password - o navegador poderá sugerir uma nova senha

`<input
    type="password"
    title="Insira uma senha com no mínimo 2 caracteres"
    placeholder="informe a sua senha"
/>
<button type="submit">Enviar</button>`

*Atributo e-mail*

- placeholder - informação no campo do que deve ser realizado
- disabled - não permite alterações
- readonly - não permite alterações, mas mantem o aspecto de ativo
- value - valor do input
- required - dado obrigatório
- multople - permite colocar mais de um e-mail separado por virgulas
- minlength - número mínimo de caracteres para o campo
- maxlength - número máximo de caracteres para o campo
- size - tamanho do campo visualmente
- pattern - expressão regular para validar o que está sendo digitado no campo .+dominio\.com\.br
- list 
  * o id de uma tag <datalist> que está no mesmo documento
  * <datalist> irá conter uma lista de valores pré definidos a fim de sugerir ao usuário, quais valores estão disponíveis
        * os valores do <datalist> que não forem compatíveis com o campo, não serão apresentados como sugestão.

`<datalist id="emailList">
  <option>julia@dominio.com.br</option>
</datalist>

<input
type="email"
placeholder="Informe seu email"
pattern=".+dominio\.com\.br"
title="Apenas e-mails dominio.com.br serão aceitos"
list="emailList"
/>
<button type="submit">Enviar</button>`

*Atributo url*

- placeholder - informação no campo do que deve ser realizado
- disabled - não permite alterações
- readonly - não permite alterações, mas mantem o aspecto de ativo
- value - valor do input
- title - acompanha as mensagens de alerta no box password
- required - dado obrigatório
- multople - permite colocar mais de um e-mail separado por virgulas
- minlength - número mínimo de caracteres para o campo
- maxlength - número máximo de caracteres para o campo
- size - tamanho do campo visualmente
- pattern 
  * expressão regular para validar o que está sendo digitado no campo
  * exemplo o usuário só poderá colocar o domínio .com.br
    * pattern=".*\.com\.br\/.*" 
- list 
  * o id de uma tag <datalist> que está no mesmo documento
  * <datalist> irá conter uma lista de valores pré definidos a fim de sugerir ao usuário, quais valores estão disponíveis
        * os valores do <datalist> que não forem compatíveis com o campo, não serão apresentados como sugestão.

`<datalist id="urlList">
        <option>https://exemplo.com.br</option>
      </datalist>

<input
  type="url"
  placeholder="https://exemplo.com.br"
  pattern=".*\.com\.br\/.*"
  title="Somente domínios .com.br serão aceitos"
  required
  list="urlList"
/>
<button type="submit">Enviar</button>`

*Demais atributos*

Consultar o site

- [MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/Input#exemplos)