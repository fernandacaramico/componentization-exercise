# Componentization exercise

Esse projeto foi iniciado com [Create React App](https://github.com/facebook/create-react-app).

## Iniciando . . .

- Clone ou faça download do projeto;
- Abra o diretório raiz no VS Code
- No terminal execute:

```shell
npm install
```

- Após terminar a instalação, execute:

```shell
npm start
```

### O que faz o comando `npm start`?

Roda a aplicação em modo de desenvolvimento.
Acesse [http://localhost:3000](http://localhost:3000) para vê-la no navegador.

_Esta página vai atualizar se você fizer alterações e em console estarão os erros._

## :zap: :zap: :zap: Adicionando props! :zap: :zap: :zap:

Fizemos os códigos abaixo em aula, mas apaguei para que vocês refaçam e vejam a mágina funcionando!

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

### Abaixo, diagrama feito em aula

Com componentes em verde, diretórios em azul e em destaque amarelo o index renderizando `<PaginaPaises />` em `<div id="root">`.

![diagrama](https://github.com/fernandacaramico/componentization-exercise/blob/main/src/assets/DiagramaComponentizacaoExercicio.jpeg?raw=true) 

## :boom: :boom: :boom: Gosta de um desafio? :boom: :boom: :boom:

Em `/src/hmtl/html-dos-filmes.html` você vai encontrar uma outra página, como abaixo. 

**O DESAFIO:** Passar este código para React! :smiley:

_Sugestão de arquivos para componentizar a página:_
- `/src/pages/PaginaFilmes.js`
- `/src/components/NavBar.js`
- `/src/components/CardFilmes.js`
- `/src/components/Footer.js`

![desafio](https://github.com/fernandacaramico/componentization-exercise/blob/main/src/assets/html-meus-filmes.png?raw=true)

