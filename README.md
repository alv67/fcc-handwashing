## Annotazioni sullo sviluppo del progetto

### 1. Preparazione del CSS
Per prima cosa vengono installati dei font di default.

Il sito di riferimento per i font è [Google Fonts](https://fonts.google.com).
Per il progetto si è scelto di utilizzare il font "[Lato](https://fonts.google.com/specimen/Lato?query=Lato#standard-styles)".

Per questo è stato inserito il comando `@import` dedicato all'interno del file `global.css` nella cartella `public`.

Inoltre si è deciso di utilizzare la libreria [Blueprint CSS](https://blueprintcss.dev) tramite il comando di installazione dedicato:

```
npm install blueprint-css --save-dev
```

e affinchè la libreria lavori correttamente occorre anche installare il pacchetto `rollup-plugin-css-only`

```
npm install --save-dev rollup-plugin-css-only
```
questo in automatico effettua anche la modifica necessaria al file `rollup.config.js`  
- aggiungendo la linea 

  `import css from 'rollup-plugin-css-only';`

- inoltre si è scelto di utilizzare il file separato `extra.css` per raggruppare i comandi css, in modo da migliorare le prestazioni dell'appilcazione

  `css({ output: 'extra.css' }),`

