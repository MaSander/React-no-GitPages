Como fazer o projeto react rodar no git hub pages

  Instale o pacote do github pages com:
    'npm install --save-dev gh-pages'

  entre no arquivo 'package.json' e inclua :
    {
     ...
     "predeploy": "npm run build",
     "deploy": "gh-pages -d build",
     ...
    }
    
   e altere em ( "homepage": '' ) a url onde a pagina vai estar,
   por exemplo: "homepage": "https://masander.github.io/TestesReact/",
    
   Então o arquivo vai ficar assim:
    "scripts": {    
       "start": "react-scripts start",
        "predeploy": "npm run build",            <---------------------
        "deploy": "gh-pages -d build",           <---------------------
       "build": "react-scripts build",
       "test": "react-scripts test",
       eject": "react-scripts eject"
      },
      
   Depois no terminal rode: 'npm run deploy'
   ele vai rodar e criar um branch para você
   
   suba para o git hub e quando for criar a ghpage escolha o branch que foi criado.

links:
  -- https://medium.com/the-andela-way/how-to-deploy-your-react-application-to-github-pages-in-less-than-5-minutes-8c5f665a2d2a
  -- https://woliveiras.com.br/posts/deploy-de-uma-aplica%C3%A7%C3%A3o-react-no-github-pages/
