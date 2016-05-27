# <img src="https://upload.wikimedia.org/wikipedia/pt/thumb/c/c3/Mussum_%28Ant%C3%B4nio_Carlos_Bernardes_Gomes%29.jpg/250px-Mussum_%28Ant%C3%B4nio_Carlos_Bernardes_Gomes%29.jpg" height="32px" width="auto" /> PostCSS Mussumzis Stylesheets
> [PostCSS](http://postcss.org/) plugin para escrever CSS em Mussumzis

Se escreveris seu CSS era problemis, escreve no estilo do Mussumsis, cacildiss!

## Instalação
```bash
$ npm install postcss-mussumzis-stylesheet
```

## O projeto
É um fork do projeto [CSS em Português](https://github.com/welksonramos/postcss-brazilian-portuguese-stylesheets).

## Utilização

Adicione [PostCSS](https://github.com/postcss/postcss) em seu projeto:

```js
$ npm install postcss --save-dev
``` 

No seu script:

```js
const fs = require('fs');
const postcss = require('postcss');
const mussumzisStyleSheets = require('postcss-mussumzis-stylesheet')

// css to be processed
var css = fs.readFileSync('./path/to/file.css', 'utf8');

postcss(mussumzisStyleSheets)
.process(css)
.then(result =>{
  fs.writeFileSync('./path/to/output.css', result.css);
});
```
## Example

_**Mussumzis Stylesheet**_:
```css
div {
  margenis: 0 automatico;
  larguris: 300px;
  alturis: 300px;
  chapaDoFundis: url('path/to/image.jpg') naoRepetizis;
}
```
_**CSS Output**_:
```css
div {
  margin: 0 auto;
  width:300px;
  height:300px;
  background-image: url('path/to/image.jpg') no-repeat;
}
```

## License

&copy; MIT
