## Estilizando o CSS, dentro de um arquivo .CSS (Projeto básico do React, após criado o projeto, 1 Opção)

Arquivo App.js

```js
import React from "react";
import "./App.css";

const App = () => {
  return (
    <div className="Nome1">
      <h1>Descrição 1</h1>
      <h2>Descrição 2</h2>
    </div>
  );
};

export default App;
```

O nome deste aquivo é App.css

```js
//Estilizando o CSS, Geral
.Nome1 {
background-color: #f8f9fa;
}

// Estilizando o css, somente no H1
.Nome1 h1 {
font-size: 32px;
color: #525252;

// Estilizando o css, somente no H2
.Nome1 h2 {
font-size: 32px;
color: #525252;
```

## Estilizando o CSS, dentro de um arquivo .CSS (Projeto básico do React, após criado o projeto, 2 Opção)

Adiconei este comando abaixo olha que facil.

```js
style={{ color: "#919191" }}
```

Vou estilizar o css, direto neste aquivo aqui, App.js.

```js
import React from "react";
import "./App.css";

const App = () => {
  return (
    <div className="Nome1">
      <h1 style={{ color: "#919191" }}>Descrição 1</h1>
      <h2 style={{ color: "#919191" }}>Descrição 2</h2>
    </div>
  );
};

export default App;
```

## Estilizando o Css, dentro de um arquivo, JavaScript (1 Opção)

Observação:
Para quem instalar está extenção, com ela você consegue estilizar o css do seu projeto, dentro de um aquivo javascript, muito utilizado nas empresas hoje em dia.

Comando para instalar o Styled-Component

```js
yarn add styled-components
```

Arquivo App.js

```js
import React from "react";

import { Title } from "./styles";
import { Paragrafo } from "./styles";
import { Botao } from "./styles";
import { Container } from "./styles";

function App() {
  return (
    <div>
      <Container>
        <Title>
          Hello Word
          <span>Texto menor</span>
        </Title>
        <Paragrafo>Oi Beto</Paragrafo>
        <Botao>Teste</Botao>
      </Container>
    </div>
  );
}

export default App;
```

Arquivo style.js

```js
import styled, { css } from "styled-components";

export const Container = styled.div`
  text-align: center;
  background-color: yellow;
`;

export const Title = styled.h1`
  color: black;

  span {
    font-size: 12px;
  }
`;

export const Paragrafo = styled.p`
  color: green;
`;

export const Botao = styled.button`
  background: transparent;
  border-radius: 3px;
  border: 2px solid palevioletred;
  color: red;
  margin: 0 1em;
  padding: 0.25em 1em;
`;
```

## Estilizando o Css, dentro de um arquivo, JavaScript (2 Opção)

Arquivo App.js

```js
import React from "react";

import * as St from "./styles";

function App() {
  return (
    <div>
      <St.Title>Hello Word</St.Title>
      <St.Paragrafo>Oi Beto</St.Paragrafo>
      <St.Botao>Teste</St.Botao>
    </div>
  );
}

export default App;
```

Arquivo style.js

```js
import styled, { css } from "styled-components";

export const Title = styled.h1`
  color: black;

  span {
    font-size: 12px;
  }
`;

export const Paragrafo = styled.p`
  color: green;
`;

export const Botao = styled.button`
  background: transparent;
  border-radius: 3px;
  border: 2px solid palevioletred;
  color: red;
  margin: 0 1em;
  padding: 0.25em 1em;
`;
```
