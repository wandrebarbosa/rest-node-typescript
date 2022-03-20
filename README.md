# rest-node-typescript
## Arquitetura REST com Node.js usando Typescript.

Iniciando uma aplicação Rest com Node.

Cria um diretorio novo.
- npm init
- touch index.js

## Instalando o TypeScript:
- npm install -g typescript
- tsc --init

-transformo meus arquivos .js para .ts e move para pasta "src"

modelo de package.json:

```
{
  "name": "ms-authentication",
  "version": "1.0.0",
  "description": "Microservice criado durante a live code com o pessoal da DIO",
  "main": "./dist/index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node ./"
    "build": "tsc -p ."
  },
  "author": "wandrebarbosa",
  "license": "ISC",
  "devDependencies": {
    "@types/node": "^17.0.21",
    "typescript": "^4.6.2"
  }
}
```

modelo de tsconfig.json:

```
/* Visit https://aka.ms/tsconfig.json to read more about this file */
{
  "compilerOptions": {
    "target": "es2019",
    "module": "commonjs",
    "moduleResolution": "node",
    "rootDir": "src",
    "typeRoots": [
      "./src/@types",
      "./node_modules/@types"
    ],
    "outDir": "./dist",
    "removeComments": true,
    "esModuleInterop": true, 
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}
```

Lembra de instalar meu typescript dentro do projeto:
```
npm install --save-dev typescript
```

E também meu @types:
```
npm install --save-dev @types/node
```

- Lembra de acrescentar no package.json a build:

    "build": "tsc -p ."

** para automatzar meu transpilador, converter meus arquivos ts para javascript na pasta "dist".

entao para executar essa conversao eu rodo o comando:

```
npm run build
```
