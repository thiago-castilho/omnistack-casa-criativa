# Anotações
* **npm i** *- Serve para instalar um novo package/dependencie*
* **npm i express** *- Serve para instalar o pacote express, que contém as funções necessárias para criar um servidor*
* **npm i nodemon** *-Serve para monitorar as alterações feitas no backend*
* **npm run {alias}** *-Serve para executar um comando pré definido no package.json*
* **npm i nunjucks** *-Serve para permitir que usemos variáveis no html*

## Utilizando o _nunjucks_
Esta biblioteca possui vários atalhos que otimizam muito a vida do desenvolvedor. Os utilizados neste projeto são:

> `{% extends "layout.html" %}` - tem a finalidade de carregar uma estrutura pré definida em uma outra página html, como na index.hmtl ou ideias.html.

> `{% set bodyId = "page-ideas" %}` - tem a finalidade de auxiliar o desenvolvedor em trocar atributos de uma classe. Neste exemplo configuramos o id da tag body como page-ideas, para que o estilo definido no css fosse atribuido devidamente. 

> `{% block title %}` - block tem como finalidade enviar um bloco completo como variável. Ao final do bloco, deve-se adicionar `{% endblock title %}` para configurar corretamente na outra página html.

> `{% include "head.html" %}` - tem como finalidade incluir tags em uma outra página hmtl. Neste exemplo, foi utilizado o head, passando as folhas de estilo do css.

> `{% for idea in ideas %}`
> <br>div class="idea"
> <br>img 
> <br>  src="{{idea.img}}" 
> <br>  alt="Coding image"
> <br>      div class="content"
> <br>           h3{{idea.title}}/h3
> <br>           p{{idea.category}}/p
> <br>           div class="description"
> <br>              {{idea.description}}
> <br>           /div
> <br>      a href="{{idea.url}}" target="_blank">Ir para a ideia/a
> <br>      /div
> <br>/div
> `{% endfor %}`
> (As tags foram removidas para fim de melhor interpretação do código. ) - Este trecho de html mostra como declarar um for, para obter os elementos de um array.


