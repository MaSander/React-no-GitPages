<h2>Como fazer o projeto react rodar no github pages<h2>

  > Instale o pacote do github pages
  ```sh
    npm install --save-dev gh-pages
  ```
  
  Entre no arquivo 'package.json' e inclua :
  ```
    {
     ...
     "predeploy": "npm run build",
     "deploy": "gh-pages -d build",
     ...
    }
  ```
    
   Altere em ( "homepage": '' ) a url onde a pagina vai estar,
   por exemplo: "homepage": "https://masander.github.io/React-no-GitPages/",
    
   Então o arquivo vai ficar assim:
   ```
    "scripts": {    
       "start": "react-scripts start",
        "predeploy": "npm run build",            <---------------------
        "deploy": "gh-pages -d build",           <---------------------
       "build": "react-scripts build",
       "test": "react-scripts test",
       eject": "react-scripts eject"
      },
   ```
      
   Depois no terminal rode:
   ```sh
   'npm run deploy'
   ```
   Ele vai rodar e criar um branch para você,
   suba para o git hub e quando for criar a ghpage escolha o branch que foi criado.

links:
  - https://medium.com/the-andela-way/how-to-deploy-your-react-application-to-github-pages-in-less-than-5-minutes-8c5f665a2d2a
  - https://woliveiras.com.br/posts/deploy-de-uma-aplica%C3%A7%C3%A3o-react-no-github-pages/
