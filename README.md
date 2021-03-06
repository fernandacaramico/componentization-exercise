# Componentization exercise

Esse projeto foi iniciado com [Create React App](https://github.com/facebook/create-react-app).

O exercício é adicionar **props** ao seu componente `/src/components/CardCountry.js` para que ele tenha diferentes nomes de países dependendo do que for "codado" ao criar o componente que será renderizado na página `/src/pages/PaginaPaises.js`.

## Como começar:

- Clone ou faça download deste repositório;
- Abra o diretório raiz no VS Code;
- No terminal execute:

```shell
npm install
```

- Após terminar a instalação, execute:

```shell
npm start
```


### O que faz o comando `npm start`?

O comando `npm start` roda a aplicação em modo de desenvolvimento.
Acesse [http://localhost:3000](http://localhost:3000) para vê-la no navegador.

_Esta página vai atualizar se você fizer alterações, e no console estarão os erros._

## ✔️✔️✔️ Resolvendo o exercício: ✔️✔️✔️

### Contextualizando

O arquivo que está em `/src/components/CardCountry.js` é de **um componente** do tipo "card" que será renderizado na página `/src/pages/PaginaPaises.js`. O card contém nome, continente, capital e idioma de um país.

### O problema:

Se quisermos adicionar vários cards (cada card de um país), teremos muita _repetição de código e retrabalho_ da maneira que o componente está desenvolvido, com os dados do país "chumbados" no código.  

### Como você resolve:

A proposta é então adicionar **props** ao seu componente `/src/components/CardCountry.js` e, na página `/src/pages/PaginaPaises.js` renderizar vários cards, cada um com um país e suas respectivas informações. Escolha quantos e quais países quiser! :)

## :zap: :zap: :zap: Resposta! :zap: :zap: :zap:

**Alerta de spoilers!** Abaixo, está a resposta para este exercício: as props adicionadas!!

(**Tente fazer por conta própria antes de sair copiando, ok?**) :wink::sparkles: _'tô de olho!!!!_


### Arquivo /src/components/CardCountry.js

```javascript
import React from 'react';

function CardCountry(props) {
    return (

        <div className="card-do-pais">
            <h1>{props.nome}</h1>
            <h2>{props.continente}</h2>
            <h3>{props.capital}</h3>
            <p>{props.idioma}</p>
        </div>
        
    );
}

export default CardCountry;
```


### Arquivo /src/pages/PaginaPaises.js

```javascript
import CardCountry from "../components/CardCountry";

function PaginaPaises() {
  return (
    <>
      <CardCountry nome="Itália" continente="Europa" capital="Roma" idioma="Italiano"/>
      <CardCountry nome="Chile" continente="América" capital="Santiago" idioma="Español" />
      <CardCountry nome="Rússia" continente="EuroÁsia" capital="Moscou" idioma="Russo" />
      <CardCountry nome="Austrália" continente="Oceania" capital="Camberra" idioma="Inglês" />
    </>
  );
}

export default PaginaPaises;

```

### Abaixo, diagrama do exercício

Com componentes em verde, diretórios em azul e em destaque amarelo o index renderizando `<PaginaPaises />` em `<div id="root">`.

![diagrama](https://github.com/fernandacaramico/componentization-exercise/blob/main/src/assets/DiagramaComponentizacaoExercicio.jpeg?raw=true)

## :boom: :boom: :boom: Gosta de um desafio? :boom: :boom: :boom:

Em `/src/hmtl/html-dos-filmes.html` você vai encontrar uma outra página, como abaixo. 

**O DESAFIO:** Passar este código para React - também com props! :smiley:

_Sugestão de arquivos para componentizar a página:_

- `/src/pages/PaginaFilmes.js`
- `/src/components/NavBar.js`
- `/src/components/CardFilmes.js` -- _adicione props aqui_
- `/src/components/Footer.js`

![desafio](https://github.com/fernandacaramico/componentization-exercise/blob/main/src/assets/html-meus-filmes.png?raw=true)

### fim!
