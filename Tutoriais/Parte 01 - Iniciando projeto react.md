# Iniciando projeto React 

1. Iniciar no terminal o seguinte comando
``` yarn create react-app Appfrontend ```

2. Excluir a linha 17 do index.html pois é exclusivo para criação de pwa

3. Deletar o arquivo manifest.json

4. Rodar ```yarn start```

5. Deletar os arquivos que não vamos usar
App.css
App.test.js
index.css
logo.svg
setup.Test.js

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