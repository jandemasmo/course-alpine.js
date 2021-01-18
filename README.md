# Curso de alpine.js

[Alpine.js](https://github.com/alpinejs/alpine/) é um micro framework que pode ajudar a
colocar um pouco de reatividade em seus projetos de forma simples e rapida.

Para acessar os exemplos você pode apenas copiar e colar em seu editor de texto. visando 
agilidade em visualizar os exemplos, todo código foi colocado inline.]

Abaixo um exemplo feito no curso.

        <!DOCTYPE html>
		<html lang="pt-br">
		<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Lesson 7 - Alpine.js - x-transition</title>
		<script src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.x.x/dist/alpine.min.js" defer></script>
		<link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet">
		</head>
		<style>
		.template{
		background-color: black;
		color: white;
		padding: 10px;
		}
		</style>
		<body>
		<!--
		Abaixo vemos como usar a diretiva transition do alpine.js
		usamos em conjunto com tailwind css
		existem 6 diretiva de trasição diferentes
		:enter	Aplicado durante toda a fase de entrada.
		:enter-start	Adicionado antes que o elemento seja inserido, removido um frame após o elemento ser inserido.
		:enter-end	Adicionado um frame após a inserção do elemento (ao mesmo tempo em que o enter-start é removido), 
		removido quando a transição/animação termina.
		:leave	Aplicado durante toda a fase de partida.
		:leave-start	Adicionado imediatamente quando uma transição de saída é acionada, removida após um frame.
		:leave-end	Adicionado um frame depois que uma transição de saída é acionada (ao mesmo tempo em que o 
		leave-start é removido), removido quando a transição/animação termina.
		-->
		<div x-data="{open: true}">
		<button x-on:click="open = !open">TOUCH</button><br><br>
		<template x-if="open" >
		<div class="template"
		x-transition:enter="transition-all ease-out duration-500"
		x-transition:enter-start="opacity-0 transform scale-75"
		x-transition:enter-end="opacity-100 transform scale-100"
		x-transition:leave="transition-all ease-in duration-500"
		x-transition:leave-start="opacity-100 transform scale-100"
		x-transition:leave-end="opacity-0 transform scale-75"
		>
		<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ex, quisquam?</p>
		</div>
		</template>
		</div>
		</body>
		</html>



## Informações sobre esse projeto

Esse curso foi feito usando como base o curso do canal 10 minutos progamando no youtube.
* [Canal 10 minutos progamando](https://www.youtube.com/c/10MinutosProgramando)

Você pode acessar um dos projetos desse curso através do link abaixo. 
Nesse projeto consumimos uma API do Rick and Morty usando o alpine.js
todo projeto foi feito inline visando facilitar o estudo e analise do funcionamento do código.
* [Project Rick and Morty](https://project-rick-and-morty-api.jandemasmo.com/)

A documentação oficial do alpine.js pode ser acessada abaixo.
* [Alpine.js](https://github.com/RichardLitt/standard-readme)


## Instalação

O alpine.js pode ser instalado usando a CDN abaixo.

`<script src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.x.x/dist/alpine.min.js" defer></script>`

Para ambiente de produção, é recomendado fixar o número da versão específico no link para evitar 
problemas inesperadas das versões mais recentes. Por exemplo, para usar a versão 2.8.0:

`<script src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.8.0/dist/alpine.min.js" defer></script>`

**Via npm:** Instale o pacote pelo npm.

`npm i alpinejs`

Incluir no script.

`import 'alpinejs';`

**Para suportar IE11** Usar os seguintes scripts.

`<script type="module" src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.x.x/dist/alpine.min.js"></script>`

`<script nomodule src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.x.x/dist/alpine-ie11.min.js" defer></script>`

O padrão acima é o padrão de módulo/nomodule que resulta num pacote moderno carregado automaticamente 
em browsers modernos e o pacote IE11 carregado automaticamente no IE11 e em outros browsers herdados.
