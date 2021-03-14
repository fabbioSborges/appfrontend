# Iniciando projeto React 

1. Iniciar no terminal o seguinte comando
``` yarn create react-app Appfrontend ```

2. Excluir a linha 17 do index.html pois é exclusivo para criação de pwa

3. Deletar o arquivo manifest.json

4. Rodar ```yarn start```

5. Deletar os arquivos que não vamos usar
* App.css
* App.test.js
* index.css
* logo.svg
* setup.Test.js

6. Alterar o arquivo src/index.js
```javascript
  import React from 'react';
  import ReactDOM from 'react-dom';
  import App from './App';

  ReactDOM.render(
    <React.StrictMode>
      <App />
    </React.StrictMode>,
    document.getElementById('root')
  );
```

7. Alterar o arquivo src/app.js

```javascrit

  function App() {
    return (
      <div className="App">
      <h1> Olá Mundo  </h1>
      </div>
    );
  }

  export default App;

```

8. Habilitar o editor config com botão direito

```
  # EditorConfig is awesome: https://EditorConfig.org

  # top-most EditorConfig file
  root = true

  [*]
  indent_style = space
  indent_size = 2
  end_of_line = lf
  charset = utf-8
  trim_trailing_whitespace = true
  insert_final_newline = true

```

9. adicionar o eslint 
``` yarn add Eslint -D ```

``` yarn eslint --init ```

* primeira opção
* Sintaxe import/export
* react
* browser
* style guide
* airbnb
* Java Script

10. Adicionar o prettier
``` yarn add prettier eslint-config-prettier eslint-plugin-prettier babel-eslint -D ```

11. Configurar o arquivo .eslintconfig

```javascript
module.exports = {
  env: {
    browser: true,
    es2021: true,
  },
  extends: [
    'plugin:react/recommended',
    'airbnb',
    'prettier',
    'prettier/react',
  ],
  parser: 'babel-eslint',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 12,
    sourceType: 'module',
  },
  plugins: [
    'react',
    'prettier',
  ],
  rules: {
    'prettier/prettier': 'error',
    'react/jsx-filename-extension': [
      'warn',
      { extensions: ['.js', '.jsx'] },
    ],
    'import/prettier-default-export': 'off',
  },
};


```

12. criar o arquivo .prettierrc

``` javascript
{
  "singleQuote": true,
  "trailingComma": "es5"
}
```